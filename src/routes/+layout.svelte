<script>
	import '../app.css'
	import { page } from '$app/stores';
	let path;
	$: path = $page.url.pathname;
</script>

<svelte:head>
	<title>AFSTATS</title>
</svelte:head>

<div class="border-b md:flex items-end border-slate-200 ">
	<a class="w-48 my-4 mx-6 inline-block" href="/">
		<img class="w-48 " alt="AFSTATS - Afghanistan Statisctics" src="/afstats-logo-2.png" />
	</a>
	<div class="items-start flex">
		<a class:bg-slate-100={path=='/'} class="ml-12 px-10 py-6 font-medium inline-block bg-slate-100 hover:bg-slate-50" href="/">
			Home
		</a>
		<a class:bg-slate-100={path=='/about'} class="px-10 py-6 font-medium inline-block hover:bg-slate-50" href="/about">
			About Us
		</a>
	</div>
</div>


<div class=" py-4 px-6">
	<slot></slot>
</div>
