<template>
  <section id="categories" class="py-16 scroll-mt-20 bg-white">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <h2 class="text-3xl font-bold text-amber-950 mb-3">
          Explore Our Oil Collections
        </h2>
        <p class="text-lg text-gray-800 max-w-2xl mx-auto">
          Discover the Perfect Oil for your machines
        </p>
      </div>

      <!-- categories -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(category, index) in categories"
          :key="index"
          class="relative group overflow-hidden rounded-lg shadow-md hover:shadow-lg transition-shadow duration-300"
        >
          <div class="h-64 overflow-hidden">
            <img
              :src="category.image"
              :alt="category.alt"
              class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
            />
          </div>
          <div
            class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent"
          >
            <div class="absolute bottom-0 left-0 p-6">
              <h3 class="text-xl font-semibold text-white">
                {{ category.title }}
              </h3>
              <p class="txt-gray-200 mt-1">{{ category.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
// import { Icon } from "@iconify/vue";
import product1 from "../assets/images/Product1.png";
import product2 from "../assets/images/Product2.png";
import product3 from "../assets/images/Product3.png";
import product4 from "../assets/images/Product4.png";
import product5 from "../assets/images/Product5.jpg";
import product6 from "../assets/images/Product6.png";

const categories = ref([
  {
    image: product1,
    title: "Automotive Oils",
    description: "High-performance oils for all types of vehicles.",
    alt: "Automotive Oils",
  },
  {
    image: product2,
    title: "Industrial Oils",
    description: "Durable oils designed for heavy machinery and equipment.",
    alt: "Industrial Oils",
  },
  {
    image: product3,
    title: "Marine Oils",
    description: "Specialized oils for marine engines and equipment.",
    alt: "Marine Oils",
  },
  {
    image: product4,
    title: "Aviation Oils",
    description: "Premium oils for aircraft engines and systems.",
    alt: "Aviation Oils",
  },
  {
    image: product5,
    title: "Engine Oils",
    description: "Safe and compliant oils for food processing.",
    alt: "Engine Oils",
  },
  {
    image: product6,
    title: "Specialty Oils",
    description: "Custom oils for unique applications and industries.",
    alt: "Specialty Oils",
  },
]);
</script>
