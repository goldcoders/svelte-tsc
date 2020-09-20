<script lang="ts">
  import Hello from '~/components/Hello.svelte';

  export let appName: string = 'Starter App';

  import Foo from './foo';

  const foo: Foo = {
    name: 'foo',
  };

  const name: string = 'Svelte, Typescript , Tailwind';
</script>

<style global>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style>

<svelte:head>
  <title>{appName}</title>
</svelte:head>

<div class="appRoot">
    <div class="bg-white">
  <div class="px-4 py-12 mx-auto text-center max-w-screen-xl sm:px-6 lg:py-16 lg:px-8">
    <h2 class="text-3xl font-extrabold tracking-tight text-gray-900 leading-9 sm:text-4xl sm:leading-10">
        {appName}
      <br>
      Using {name} , foo load === {foo.name}
      <Hello/>
    </h2>
    <div class="flex justify-center mt-8">
      <div class="inline-flex shadow rounded-md">
        <a href="#" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-white bg-indigo-600 border border-transparent leading-6 rounded-md hover:bg-indigo-500 focus:outline-none focus:shadow-outline transition duration-150 ease-in-out">
          Get started
        </a>
      </div>
      <div class="inline-flex ml-3">
        <a href="#" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-indigo-700 bg-indigo-100 border border-transparent leading-6 rounded-md hover:text-indigo-600 hover:bg-indigo-50 focus:outline-none focus:shadow-outline focus:border-indigo-300 transition duration-150 ease-in-out">
          Learn more
        </a>
      </div>
    </div>
  </div>
</div>
</div>
