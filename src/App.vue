<template>
	<div class="blocs-container">
		<div class="blocs">
			<RandomWallpaper />
		</div>
	</div>
	<svg class="bokeh" viewBox="0 0 10 10" xmlns="http://www.w3.org/2000/svg">

		<circle cx="10%" cy="85%" r="75%" />
		<circle cx="45%" cy="50%" r="15%" />
		<circle cx="85%" cy="35%" r="30%" />
		<circle cx="60%" cy="85%" r="20%" />
		<circle cx="45%" cy="50%" r="30%" />
		<circle cx="35%" cy="25%" r="20%" />
		<circle cx="90%" cy="-25%" r="35%" />
		<circle cx="-15%" cy="30%" r="30%" />
		<circle cx="65%" cy="85%" r="55%" />
		<circle cx="45%" cy="50%" r="20%" />
	</svg>
</template>

<script>
import RandomWallpaper from './components/RandomWallpaper.vue'

export default {
	name: 'App',
	components: {
		RandomWallpaper
	}
}
</script>

<style>
html,
body {
	margin: 0;
	padding: 0;
	box-sizing: content-box
}

#app {
	background-color: #000000;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
	padding: 0;
	margin: 0;
	font-family: Avenir, Helvetica, Arial, sans-serif;
	width: 100vw;
	height: 100vh;
	box-sizing: border-box;
	background-image: url('/src/assets/background.jpg');
	background-size: cover;
	padding: 20px;
	display: flex;
}

.blocs-container {
	width: 100%;
	height: 100%;
	background: rgba(16, 21, 61, 0.5);
	backdrop-filter: blur(10px);
	-webkit-backdrop-filter: blur(10px);
	border-radius: 15px;
	box-shadow: 0 0.5px 0 1px rgba(255, 255, 255, 0.13) inset, 0 1px 0 0 rgba(255, 255, 255, 0.1) inset, 0 4px 16px rgba(0, 0, 0, 0.2);
	z-index: 1;
}

.blocs {
	display: flex;
	margin: 10px;
}

body {
	overflow: hidden;
	background-color: #013;
}

.bokeh {
	height: 100vh;
	width: 100vw;
	background-color: #124;
	position: fixed;
	top: 0;
	bottom: 0;
	left: 0;
	right: 0;
	filter: blur(50px);
	transform: translateZ(0);
	backface-visibility: hidden;
	opacity: 0.3;
}

.bokeh circle {
	animation: rotate 26s linear infinite;
	fill: #124;
	opacity: 0.43;
	transform-origin: 50%;
}

.bokeh circle:nth-child(2n) {
	fill: #614;
	transform-origin: 20% 110%;
	animation-delay: -3s;
	animation-duration: 14.1316s;
	opacity: 0.2;
}

.bokeh circle:nth-child(3n) {
	opacity: 0.65;
	fill: #469;
	transform-origin: 70% 30%;
	animation-delay: -11.5s;
	animation-duration: 17.9998s;
}

.bokeh circle:nth-child(4n) {
	fill: #c63;
	transform-origin: 110% 70%;
	animation-delay: -2s;
	animation-duration: 14.77996s;
}

.bokeh circle:nth-child(5n) {
	fill: #266;
	transform-origin: 30% 40%;
}

.bokeh circle:nth-child(6n) {
	fill: #124;
	transform-origin: -10% 80%;
	animation-delay: -17.8s;
}

.bokeh circle:nth-child(7n) {
	fill: #614;
	transform-origin: 70% -10%;
}

.bokeh circle:nth-child(8n) {
	fill: #c63;
	transform-origin: -30% 50%;
	animation-delay: -12.4s;
}

@keyframes rotate {
	0% {
		transform: rotate(0deg);
	}

	100% {
		transform: rotate(360deg);
	}
}
</style>
