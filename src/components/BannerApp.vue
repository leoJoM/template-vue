<script setup lang="ts">
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
import { useAuthStore } from '@/stores/Auth'

const userStore = useAuthStore()
const User = userStore.user?.Nombre

// inicializar libreria flowBite
onMounted(() => {
	initFlowbite()
})
</script>

<template>
	<div
		class="w-full bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
	>
		<section
			class="bg-white dark:bg-gray-900 bg-[url('https://flowbite.s3.amazonaws.com/docs/jumbotron/hero-pattern.svg')] dark:bg-[url('https://flowbite.s3.amazonaws.com/docs/jumbotron/hero-pattern-dark.svg')]"
		>
			<div
				class="py-8 px-4 mx-auto max-w-screen-xl text-center lg:py-16 z-10 relative"
			>
				<a
					href="#"
					class="inline-flex justify-between items-center py-1 px-1 pe-4 mb-7 text-sm text-blue-700 bg-blue-100 rounded-full dark:bg-blue-900 dark:text-blue-300 hover:bg-blue-200 dark:hover:bg-blue-800"
				>
					<span
						class="text-xs bg-blue-600 rounded-full text-white px-4 py-1.5 me-3"
						>Nuevo</span
					>
					<span class="text-sm font-medium">Portal</span>
					<svg
						class="w-2.5 h-2.5 ms-2 rtl:rotate-180"
						aria-hidden="true"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 6 10"
					>
						<path
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="m1 9 4-4-4-4"
						/>
					</svg>
				</a>
				<h1
					class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-gray-900 md:text-5xl lg:text-6xl dark:text-white"
				>
					MCD ™
				</h1>
				<p
					class="mb-8 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 lg:px-48 dark:text-gray-200"
				>
					Hola
					<span class="text-blue-500 font-semibold">{{ User }}</span
					>, bienvenido a la aplicacion de MCD de 
					Tiendas Daka, la tienda mas feliz de venezuela.
				</p>
				<form class="w-full max-w-md mx-auto">
					<label
						for="default-email"
						class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white"
						>Email sign-up</label
					>
					<div class="relative">
						<div
							class="absolute inset-y-0 rtl:inset-x-0 start-0 flex items-center ps-3.5 pointer-events-none"
						>
							<svg
								class="w-4 h-4 text-gray-500 dark:text-gray-400"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								fill="currentColor"
								viewBox="0 0 20 16"
							>
								<path
									d="m10.036 8.278 9.258-7.79A1.979 1.979 0 0 0 18 0H2A1.987 1.987 0 0 0 .641.541l9.395 7.737Z"
								/>
								<path
									d="M11.241 9.817c-.36.275-.801.425-1.255.427-.428 0-.845-.138-1.187-.395L0 2.6V14a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V2.5l-8.759 7.317Z"
								/>
							</svg>
						</div>
						<input
							type="email"
							id="default-email"
							class="block w-full p-4 ps-10 text-sm text-gray-900 border border-gray-300 rounded-lg bg-white focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-800 dark:border-gray-700 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
							placeholder="Enter your email here..."
							required
						/>
						<button
							type="submit"
							class="text-white absolute end-2.5 bottom-2.5 bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
						>
							Sign up
						</button>
					</div>
				</form>
			</div>
			<div
				class="bg-gradient-to-b from-blue-50 to-transparent dark:from-blue-900 w-full h-full absolute top-0 left-0 z-0"
			></div>
		</section>
	</div>
</template>
