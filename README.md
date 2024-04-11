# Concepts/Self notes

How many heads inside an attention block? 
- How many distinct ways can our context change the semantics of tokens? How complex are the interactions in our problem's modality?

Any downsides to spamming heads besides computing cost and memory usage?
- Overfitting? Is one now learning noise/idiosyncrasies from the training data or is it capturing legit semantic changes? Meaning, is the model catching the semantic shift of tokens caused by context or by distribution?

Main problems with transformers?
- Quadratic scaling from context windows (long sequences melts memory and inference times, inference times are linearly affected by KV).

Pros of new architecture Hawk:
- Local attention accurately models the recent past while the recurrent layer can transmit info across long sequences. Uses the same residual pattern and MLP block as the transformers but Griffin uses mix of recurrent and MQA blocks (hybrid?).
