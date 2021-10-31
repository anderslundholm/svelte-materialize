<script>
	import { set_input_type } from "svelte/internal";
	let firstName = "";
	let lastName = "";
	let favicon = "favicon.png";
	let counter = 0;
	let checked = true;
	const incrementCounter = () => {
		counter += 1;
	};
	const handleInput = (event) => {
		name = event.target.value;
	};
	const resetName = () => {
		firstName = "";
		lastName = "";
	};
	$: fullName =
		(firstName || lastName) === "" ? "Unknown" : `${firstName} ${lastName}`;
	$: console.log(fullName);
</script>

<div class="container row">
	<h1>Hello {fullName}</h1>
	<h3>Counter: {counter}</h3>
	<div class="section">
		<button class="btn waves-effect waves-light" on:click={incrementCounter}
			>Add to Counter<i class="material-icons right">add_circle_outline</i
			></button
		>
		<button class="btn waves-effect waves-light" on:click={resetName}
			>Reset name!<i class="material-icons right">refresh</i></button
		>
	</div>

	<form class="col s12">
		<div class="row">
			<div class="input-field col s12">
				<select>
					<optgroup label="team 1">
						<option value="1">Option 1</option>
						<option value="2">Option 2</option>
					</optgroup>
					<optgroup label="team 2">
						<option value="3">Option 3</option>
						<option value="4">Option 4</option>
					</optgroup>
				</select>
				<label for="optgroups">Optgroups</label>
			</div>
		</div>
		<div class="row">
			<div class="input-field col s6">
				<label for="firstname">First name</label>
				<input type="text" bind:value={firstName} />
			</div>
		</div>

		<div class="row">
			<div class="input-field col s6">
				<label for="lastname">Last name</label>
				<input type="text" bind:value={lastName} />
			</div>
		</div>
		<div class="section">
			<input type="checkbox" bind:checked />
		</div>

		<div class="section">
			<button
				class="btn waves-effect waves-light"
				type="submit"
				name="action"
				>Submit
				<i class="material-icons right">send</i>
			</button>
		</div>
	</form>
	<div class="carousel">
		<a class="carousel-item" href="#two!"
			><img
				src="https://images.unsplash.com/photo-1558383331-f520f2888351?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"
				alt="1"
			/></a
		>
		<a class="carousel-item" href="#three!"
			><img
				src="https://images.unsplash.com/photo-1600716051809-e997e11a5d52?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80"
				alt="2"
			/></a
		>
		<a class="carousel-item" href="#four!"
			><img
				src="https://images.unsplash.com/photo-1561336313-0bd5e0b27ec8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"
				alt="3"
			/></a
		>
		<a class="carousel-item" href="#five!"
			><img
				src="https://images.unsplash.com/photo-1579353977828-2a4eab540b9a?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8c2FtcGxlfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80"
				alt="4"
			/></a
		>
	</div>

	<table class="striped">
		<thead>
			<tr>
				<th>Name</th>
				<th>Item Name</th>
				<th>Item Price</th>
			</tr>
		</thead>

		<tbody>
			<tr>
				<td>Alvin</td>
				<td>Eclair</td>
				<td>$0.87</td>
			</tr>
			<tr>
				<td>Alan</td>
				<td>Jellybean</td>
				<td>$3.76</td>
			</tr>
			<tr>
				<td>Jonathan</td>
				<td>Lollipop</td>
				<td>$7.00</td>
			</tr>
		</tbody>
	</table>
</div>

<style>
</style>
