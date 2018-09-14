# bonus-assignment-ell881
Bonus assignment for Ankur Sharma 2015CS50278, ELL881

For each sentence, return a a tuple with two entries

words in the sentence
characters from the first word in sentence.
This is how sample output should look like for a batch size of 2:

 array([[b'anarchism', b'is', b'a', b'political', b'philosophy', b'that',
         b'advocates', b'self-governed', b'societies', b'based', b'on',
         b'voluntary', b'institutions', b'.', b'', b'', b'', b'', b'',
         b'', b'', b'', b'', b'', b''],
        [b'these', b'are', b'often', b'described', b'as', b'stateless',
         b'societies', b',', b'although', b'several', b'authors', b'have',
         b'defined', b'them', b'more', b'specifically', b'as',
         b'institutions', b'based', b'on', b'non-hierarchical', b'or',
         b'free', b'associations', b'.']], dtype=object)>,
 <tf.Tensor: id=242, shape=(2, 9), dtype=string, numpy=
 array([[b'a', b'n', b'a', b'r', b'c', b'h', b'i', b's', b'm'],
        [b't', b'h', b'e', b's', b'e', b'', b'', b'', b'']], dtype=object)>)
        
 
Hint:
1. use tf.string_split with delimiter as ''
2. tf.string_split returns sparse tensor, Use tf.sparse_tensor_to_dense to convert to a dense tensor, use default_value of UNK
3. You would need to convert the char tensor to 1D. use tf.squeeze with axis=0
