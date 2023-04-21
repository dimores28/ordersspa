<template>
   <header class="header">
      <div class="header__container">
         <div class="header__logo">
            <img src="img/logo.png" alt="logo" />
            <p>inventory</p>
         </div>

         <div class="header__search">
            <div class="header__search_icon">
               <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 16 16">
                  <path
                     d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z" />
               </svg>
            </div>
            <input type="text" id="search" placeholder="search" />
         </div>

         <div class="header__date date">
            <div class="date__icon">
               <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 16 16">
                  <path
                     d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5zM2 2a1 1 0 0 0-1 1v1h14V3a1 1 0 0 0-1-1H2zm13 3H1v9a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V5z" />
                  <path
                     d="M11 7.5a.5.5 0 0 1 .5-.5h1a.5.5 0 0 1 .5.5v1a.5.5 0 0 1-.5.5h-1a.5.5 0 0 1-.5-.5v-1z" />
               </svg>
            </div>
            <p class="date__day">Today</p>
            <time class="date__body">
               <div class="date__number">12 MAR, 2017</div>
               <div class="date__time">
                  <div>
                     <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="16"
                        height="16"
                        viewBox="0 0 16 16">
                        <path
                           d="M8 3.5a.5.5 0 0 0-1 0V9a.5.5 0 0 0 .252.434l3.5 2a.5.5 0 0 0 .496-.868L8 8.71V3.5z"
                           fill="#198754" />
                        <path
                           d="M8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16zm7-8A7 7 0 1 1 1 8a7 7 0 0 1 14 0z"
                           fill="#198754" />
                     </svg>
                  </div>
                  <span>17:20</span>
               </div>
            </time>
         </div>
      </div>
   </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
   padding: 14px 20px 8px 20px;
   box-shadow: rgba(0, 0, 0, 0.25) 0px 14px 28px,
      rgba(0, 0, 0, 0.22) 0px 10px 10px;
   // .header__container

   &__container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
   }

   // .header__logo

   &__logo {
      max-width: 45px;
      display: flex;
      align-items: center;
      gap: 14px;

      @media (max-width: 550px) {
         max-width: 35px;
      }

      img {
         width: 100%;
         height: auto;
      }

      p {
         color: #198754;
         font-weight: bold;
         font-size: 20px;
         text-transform: uppercase;

         @media (max-width: 858px) {
            opacity: 0;
         }
      }
   }

   // .header__search

   &__search {
      max-width: 300px;
      flex: 1 1 auto;
      position: relative;

      &_icon {
         display: none;
         text-align: right;
         margin-right: 4px;

         svg {
            width: 28px;
            height: 28px;
         }

         @media (max-width: 550px) {
            display: block;
         }
      }

      input {
         font-size: 18px;
         padding: 6px 10px;
         width: 100%;
         background: rgba(255, 255, 255, 0.7);
         border-radius: 4px;
         box-shadow: inset 0 2px 10px 1px rgba(0, 0, 0, 0.3),
            inset 0 0 0 60px rgba(0, 0, 0, 0.1), 0 1px rgba(255, 255, 255, 0.08);

         &:focus {
            outline: none;
            box-shadow: inset 0 1px 3px 1px rgba(0, 0, 0, 0.7),
               inset 0 0 0 60px rgba(0, 0, 0, 0),
               0 1px rgba(255, 255, 255, 0.08);
         }

         @media (max-width: 550px) {
            display: none;
         }
      }
   }

   // .header__date

   &__date {
      flex-shrink: 0;
   }
}
.date {
   @media (max-width: 550px) {
      display: flex;
      gap: 14px;
      align-items: center;
   }

   &__icon {
      display: none;

      svg {
         width: 28px;
         height: 28px;
      }

      @media (max-width: 550px) {
         display: block;
      }
   }

   &__day {
      margin-bottom: 12px;

      @media (max-width: 550px) {
         display: none;
      }
   }

   // .date__body

   &__body {
      display: flex;
      gap: 14px;
   }

   // .date__number

   &__number {
      @media (max-width: 550px) {
         display: none;
      }
   }

   // .date__time

   &__time {
      display: flex;
      gap: 8px;
   }
}
</style>
