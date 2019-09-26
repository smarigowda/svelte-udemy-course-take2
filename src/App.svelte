<script>
  export let name;
  export let age;
  const handleClick = () => {
    console.log("button clicked");

    age = Math.floor(Math.random() * 40);
  };
</script>

<style lang="scss">
  $color: red;

  h1 {
    color: $color;
    & a {
      color: green;
    }
  }
  .container {
	  & button {
		  color: blueviolet;
	  }
  }
</style>

<h1>Hello {name}, your age is {age}!</h1>
<div class="container">
  <button on:click={handleClick}>Change Age</button>
</div>
