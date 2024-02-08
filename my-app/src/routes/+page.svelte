<div class="container">
	<h2 class="hint">Hey Gracy , I hope you're having a fine day 😀 <br> I was thinking about you and so I have created this small website for you which is hosted at gracy.vercel.app  <br><br> I know exams are coming close but i wanted to share a story and small poem dedicated to you. If you are unable to solve the question no problem , the poetry is at <a href="/poetry"> here (click on this link)</a>
		also i am proud of my poetry , i think <br> But i would really like if you read just a bit of animal farm . I am giving you a small question which you can easily find in the book  <br>
	<br><br> this question can easily be searched on internet but i know that you wont do that :) <br> <br>
	<strong>Question:</strong> who claimed to know the existence of a mysterious country called Sugarcandy Mountain <br> <strong>Hint : </strong> if you write the correct word , the input box would turn green & button would also change.</h2>
	
	
	
	
	
	<input type="text" id="inputBox" bind:value="{inputValue}" placeholder="Type something..." class="full-width"  class:green-border={inputValue === 'moses' || inputValue === 'Moses'}>
	<button class="full-width" on:click={handleButtonClick} class:green-button={ (inputValue.trim().toLowerCase() === 'moses')}>{buttonText} </button>
  </div>

<style>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height:  100vh;
  }
  .green-border {
    outline: 2px solid #16db65;/* Apply a green border */
  }
  .green-button {
	background-color: #16db65;
  }

  /* Hint Styles */
  .hint {
    text-align: center;
    margin-bottom:  1rem; /* Space between the hint and the input box */
  }
  
  /* Input Group Styles */
  .input-group {
    display: flex;
    justify-content: center;
    align-items: center;
    gap:  1rem; /* Space between the input and button */
  }

.full-width {
    width:  100%;
    box-sizing: border-box;
  }
  
  /* Button Styles */
  button {
    display: block; /* Makes the button a block element, so it takes up the full width and appears below the input field */
    padding:  0.5rem;
    background-color: #007BFF;
    color: white;
    border: none;
    border-radius:  4px;
    cursor: pointer;
    margin-top:  1rem; /* Adds some space above the button */
  }

  
</style>
<script>
	import { goto } from '$app/navigation';
  
	let inputValue = ''; // Variable to hold the input value
	let buttonText='See If Its the correct answer 😀'
  
	// Function to handle the button click
	function handleButtonClick() {
	  if (inputValue.trim().toLowerCase() === 'moses') {
		goto('/poetry'); // Navigate to the /poetry page
		
	  } 
	}
	$: {
    if (inputValue.trim().toLowerCase() === 'moses') {
      buttonText = 'Yes, this is the correct answer';
    } else {
      buttonText = 'See If Its the correct answer 😀';
    }
  }
  </script>
  
