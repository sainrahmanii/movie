<template>
  <div>
    <header
      class="fixed top-0 left-0 z-10 flex items-center w-full bg-transparent lg:px-32 backdrop-blur-md"
    >
      <div class="container">
        <div class="relative flex items-center justify-between">
          <div>
            <router-link
              to="/"
            >
              <Image />
            </router-link>
          </div>
          <div class="flex items-center">
            <button
              @click="mobileMenu = !mobileMenu"
              class="absolute block right-4 lg:hidden"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-5 h-5"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M3.75 6.75h16.5M3.75 12h16.5M12 17.25h8.25"
                />
              </svg>
            </button>
            <nav
              id="nav-menu"
              class="absolute w-full py-5 bg-white rounded-lg shadow-lg md:pl-5 right-4 top-full lg:block lg:static lg:bg-transparent lg:max-w-full lg:shadow-none lg:rounded-none"
              :class="{ hidden: mobileMenu }"
            >
              <ul class="block lg:flex">
                <li class="group">
                  <a
                    href="#home"
                    class="flex py-2 mx-4 text-base font-medium text-white group-hover:text-slate-500"
                    >Movies</a
                  >
                </li>
                <li class="group">
                  <a
                    href="#about"
                    class="flex py-2 mx-4 text-base font-medium text-white group-hover:text-slate-500"
                    >Now Playing</a
                  >
                </li>
                <li class="group">
                  <a
                    href="#portfolio"
                    class="flex py-2 mx-4 text-base font-medium text-white group-hover:text-slate-500"
                    >Upcoming</a
                  >
                </li>
              </ul>
            </nav>
          </div>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
import { ref } from "vue";
const mobileMenu = ref(true);
</script>
