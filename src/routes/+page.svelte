<script lang="ts">
	import { FirebaseFirestore } from '@capacitor-firebase/firestore';

	const addDocument = async () => {
		await FirebaseFirestore.addDocument({
			reference: 'users',
			data: {
				first: 'Alan',
				last: 'Turing',
				born: 1912
			}
		});
	};
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<button on:click={addDocument}>Add User Document</button>
