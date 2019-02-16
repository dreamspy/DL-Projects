## text => ./data/simpsons/moes\_tavern\_lines.txt
| code|description|
|----|----|
|/n| New line|
|/n/n | New Scene|

#### Excerpt from text, string variable



>"Moe_Szyslak: (INTO PHONE) Moe's Tavern. Where the elite meet to drink.\nBart_Simpson: Eh, yeah, hello, is Mike there? Last name, Rotch.\nMoe_Szyslak: (INTO PHONE) Hold on, I'll check. (TO BARFLIES) Mike Rotch. Mike Rotch. Hey, has anybody seen Mike Rotch, lately?\nMoe_Szyslak: (INTO PHONE) Listen you little puke. One of these days I'm gonna catch you, and I'm gonna carve my name on your back with an ice pick.\nMoe_Szyslak: What's the matter Homer? You're not your normal effervescent self.\nHomer_Simpson: I got my problems, Moe. Give me another one.\nMoe_Szyslak: Homer, hey, you should not drink to forget your problems.\nBarney_Gumble: Yeah, you should only drink to enhance your social skills.\n**\n\n**Moe_Szyslak: Ah, isn't that nice. Now, there is a politician who cares.\nBarney_Gumble: If I ever vote, it'll be for him. (BELCH)\n\n\nBarney_Gumble: Hey Homer, how's your neighbor's store doing?\nHomer_Simpson: Lousy. He just sits there all day. He'd have a great job if he didn't own the place. (CHUCKLES)\n"


## scenes
#### excerpt from scenes, list of strings
```
Moe_Szyslak: (INTO PHONE) Moe's Tavern. Where the elite meet to drink.
Bart_Simpson: Eh, yeah, hello, is Mike there? Last name, Rotch.
Moe_Szyslak: (INTO PHONE) Hold on, I'll check. (TO BARFLIES) Mike Rotch. Mike Rotch. Hey, has anybody seen Mike Rotch, lately?
Moe_Szyslak: (INTO PHONE) Listen you little puke. One of these days I'm gonna catch you, and I'm gonna carve my name on your back with an ice pick.
Moe_Szyslak: What's the matter Homer? You're not your normal effervescent self.
Homer_Simpson: I got my problems, Moe. Give me another one.
Moe_Szyslak: Homer, hey, you should not drink to forget your problems.
Barney_Gumble: Yeah, you should only drink to enhance your social skills.

Moe_Szyslak: Ah, isn't that nice. Now, there is a politician who cares.
Barney_Gumble: If I ever vote, it'll be for him. (BELCH)

Barney_Gumble: Hey Homer, how's your neighbor's store doing?
Homer_Simpson: Lousy. He just sits there all day. He'd have a great job if he didn't own the place. (CHUCKLES)
Moe_Szyslak: (STRUGGLING WITH CORKSCREW) Crummy right-handed corkscrews! What does he sell?
Homer_Simpson: Uh, well actually, Moe...
HOMER_(CONT'D: I dunno.
```

## Functions 
### ```create_lookup_tables(text):```
Words 2 INT

```
def create_lookup_tables(text):
	return vocab_to_int, int_to_vocab
```

### ```get_inputs()```
Create TF Placeholders 

```
def get_inputs():
    return input, targets,learning_rate
```

### ```get_init_cell``` : Build RNN Cell and Initialize
Stack one or more [`BasicLSTMCells`](https://www.tensorflow.org/api_docs/python/tf/contrib/rnn/BasicLSTMCell) in a [`MultiRNNCell`](https://www.tensorflow.org/api_docs/python/tf/contrib/rnn/MultiRNNCell).

	def get_init_cell(batch_size, rnn_size):
	    return Outputs, FinalState

### ```get_embed()```
???????????????

	def get_embed(input_data, vocab_size, embed_dim):
	    """
	    Create embedding for <input_data>.
	    :param input_data: TF placeholder for text input.
	    :param vocab_size: Number of words in vocabulary.
	    :param embed_dim: Number of embedding dimensions
	    :return: Embedded input.
	    """
	    return embeddedInput


## ```build_rnn(cell, inputs)```

	def build_rnn(cell, inputs):
	    """
	    Create a RNN using a RNN Cell
	    :param cell: RNN Cell
	    :param inputs: Input text data
	    :return: Tuple (Outputs, Final State)
	    """
	    # TODO: Implement Function
	    return None, None
	    
## ```build_nn(cell, rnn_size, input_data, vocab_size, embed_dim)```
	def build_nn(cell, rnn_size, input_data, vocab_size, embed_dim):
	    """
	    Build part of the neural network
	    :param cell: RNN cell
	    :param rnn_size: Size of rnns
	    :param input_data: Input data
	    :param vocab_size: Vocabulary size
	    :param embed_dim: Number of embedding dimensions
	    :return: Tuple (Logits, FinalState)
	    """
	    # TODO: Implement Function
	    return Logits, FinalSTate
	 	
## ```get_batches(int_text, batch_size,seq_length)```
	def get_batches(int_text, batch_size, seq_length):
	    """
	    Return batches of input and target
	    :param int_text: Text with the words replaced by their ids
	    :param batch_size: The size of batch
	    :param seq_length: The length of sequence
	    :return: Batches as a Numpy array
	    """
	    # TODO: Implement Function
	    return None   
	    