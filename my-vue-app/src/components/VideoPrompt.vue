<template>
  <div class="text-white py-12 flex flex-col items-center" ref="videoPromptContainer">
    <h2 class="text-4xl font-bold mb-6">Ready to Analyze Your Dance?</h2>
    <p class="text-lg mb-8 text-gray-400">
      Upload your dance video below to get started with AI-powered analysis.
    </p>
    <button @click="$scrollTo('#video-prompt')" class="border border-white text-white px-6 py-3 rounded-full hover:bg-white hover:text-black">
      Upload Video
    </button>
  </div>
</template>

<script>
import { gsap } from 'gsap';

export default {
  name: 'VideoPrompt',
  mounted() {
    this.animateVideoPrompt();
  },
  methods: {
    animateVideoPrompt() {
      // Apply a 6-second ease-in animation to the container
      gsap.to(this.$refs.videoPromptContainer, {
        duration: 6, // Duration of the animation
        opacity: 1, // Target opacity
        y: 0, // Move to its original position
        ease: 'power2.in', // Ease-in effect
        startAt: { opacity: 0, y: 50 } // Starting values
      });
    }
  }
};
</script>

<style scoped>
/* Add additional styling if needed */
</style>
