<script>
let T = '';
let input = '';
let finesse = '';

const calculate = (T, input, finesse) => {
	[T, input, finesse] = [T, input, finesse].map(parseFloat);
	return T * input * Math.pow(finesse, 2) / Math.pow(Math.PI, 2);
}
</script>

<h1>Intracavity Power</h1>

<p>The intracavity power is given by P = T * P_1 * F^2 / pi^2 </p>
<input bind:value={input} placeholder="enter input power (W)" />
<input bind:value={finesse} placeholder="enter finesse" />
<input bind:value={T} placeholder="enter transmission" />

<p>The intracavity power is: {calculate(T,input,finesse) || 0} W </p>
