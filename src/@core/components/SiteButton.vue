<script setup>
defineProps({
  outlined: {
    type: Boolean,
    default: false
  }
})

const primaryBtnClasses = 'bg-primary text-white rounded-2lg'
const outlineBtnClasses = 'bg-transparent rounded-4xl outline outline-2 outline-primary text-white hover:outline-white'
</script>

<template>
  <button
      :class="[outlined ? outlineBtnClasses : primaryBtnClasses]"
      class="text-sm sm:text-base lg:text-lg 2xl:text-xl 3xl:text-2xl font-bold px-3 sm:px-5 py-2 lg:px-6 3xl:px-9.5 3xl:py-5"
  >
    <slot />
  </button>
</template>

<style scoped>
button{
  transition: all .3s ease-in;
}
button.bg-primary{
  background: radial-gradient(90.62% 183.93% at 50.15% 0%, rgba(255, 255, 255, 0.37) 0%, rgba(0, 123, 167, 0.00) 100%), theme('colors.primary');
}
button.bg-primary:hover{
  box-shadow: 0 3px 9px 1px theme('colors.primary');
  transform: translateY(-3px);
}
</style>