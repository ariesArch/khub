<template>
      <nav class="relative container mx-auto p-6">
        <!-- Flex Container For All Items -->
        <div class="flex items-center justify-between">
            <img src="../../assets/images/icons8-bbb-96.svg" alt="" class="z-40 w-14 h-14 md:w-28 md:h-28" />
            <!--Menu -->
            <div class="hidden items-center space-x-10 uppercase lg:flex">
                <a href="#home" class="text-white no-underline hover:text-blue-500 ">Home</a>
                <a href="#about" class="text-white no-underline hover:text-blue-500">About Us</a>
                <a href="#service" class="text-white no-underline hover:text-blue-500">Our Services</a>
                <a href="#works" class="text-white no-underline hover:text-blue-500">Our Works</a>
                <a href="#contactus"
                    class="px-4 py-2  no-underline text-white bg-blue-500 border-2 rounded-lg shadow-md hover:text-blue-500 hover:bg-white">Conatct
                    Us</a>
            </div>

            <div id="mobilemenu" class="md:hidden">
                <!-- Hamburger Button -->
                <button class="mobilemenu-btn" v-on:click="navOpen=!navOpen" v-bind:class="{active:navOpen, fixed:navOpen}">
                            <span class="top"></span>
                            <span class="mid"></span>
                            <span class="bottom"></span>
                </button>
                    
                <!-- Mobile Menu -->
                    <div v-show="navOpen" id="menu"
                    class="fixed inset-0 z-20 flex-col items-center self-end w-full h-full m-h-screen px-6 py-1 pt-24 pb-4 tracking-widest text-black uppercase divide-y divide-gray-500 opacity-90 bg-gray-300">
                        <div class="w-full py-3 text-center">
                            <a href="#home" class="block hover:text-blue-500">Home</a>
                        </div>
                        <div class="w-full py-3 text-center">
                            <a href="#about" class="block hover:text-blue-500">About Us</a>
                        </div>
                        <div class="w-full py-3 text-center">
                            <a href="#service" class="block hover:text-blue-500">Our Services</a>
                        </div>
                        <div class="w-full py-3 text-center">
                            <a href="#works" class="block hover:text-blue-500">Our Works</a>
                        </div>
                        <div class="w-full py-3 text-center">
                            <a href="#contactus" class="block hover:text-blue-500">Contact Us</a>
                        </div>
                    </div>
            </div>
        </div>
       
    </nav>
</template>

<script>
export default {
    data() {
		return {
      navOpen: false,
	};
},
}
</script>

<style>

#mobilemenu .mobilemenu-btn {
  display: block;
  width: 50px;
  height: 50px;
  border: none;
  position: relative;
  z-index: 100;
  cursor: pointer;
  outline: none;
}
#mobilemenu .mobilemenu-btn.fixed{
  position: fixed;
  top: 30px;
  right: 25px;
}
#mobilemenu .mobilemenu-btn span {
  display: block;
  width: 25px;
  height: 2px;
  margin: auto;
  background: white;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  transition: all 0.4s ease;
}
#mobilemenu .mobilemenu-btn span.top {
  transform: translateY(-8px);
}
#mobilemenu .mobilemenu-btn span.bottom {
  transform: translateY(8px);
}
#mobilemenu .mobilemenu-btn.active .top {
  transform: rotate(-45deg);
}
#mobilemenu .mobilemenu-btn.active .mid {
  transform: translateX(-20px) rotate(360deg);
  opacity: 0;
}
#mobilemenu .mobilemenu-btn.active .bottom {
  transform: rotate(45deg);
}
</style>