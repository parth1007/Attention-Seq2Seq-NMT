## Attention-Seq2Seq-nmt
In this project I have created a german to english language translator implemented using Attention mechanism over a Seq2Seq model.
It uses a bidirectional GRU mechanism for encoder part and unidirectional GRU for decoder. The Attention mechanism applied reduces the problem of information compression by allowing the decoder to "look back" at the input sentence by creating context vectors that are weighted sums of the hidden states of encoder. Attention mechanism calculates the weights for this weighted sum and helps the decoder learn to pay attention to the most useful words in the input sentence.

Reference Research Paper [Link](https://www.researchgate.net/publication/265252627_Neural_Machine_Translation_by_Jointly_Learning_to_Align_and_Translate)

The Attention mechanism is further improved adding 
<ul>
<li>Packed padded sequences (allow us to only process the non-padded elements of our input sentence with our RNN)</li>
<li>Masking (forces the model to ignore attention over padded elements)</li>
</ul>

The Model results the Bleu score of ~29 whereas the simple Seq2Seq model resulted the Bleu Score of 19.

Libraries used : Pytorch, TorchText, matplotlib, spaCy
