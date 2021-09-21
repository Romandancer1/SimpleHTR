test model

> python main.py

> python main.py --img_file ../data/line.png

Follow these instructions to integrate word beam search decoding:

Clone repository CTCWordBeamSearch
Compile and install by running pip install . at the root level of the CTCWordBeamSearch repository<br>
Specify the command line option --decoder wordbeamsearch when executing main.py to actually use the decoder<br>
The dictionary is automatically created in training and validation mode by using all words contained in the IAM dataset (i.e. also including words from validation set) and is saved into the file data/corpus.txt. Further, the manually created list of word-characters can be found in the file model/wordCharList.txt. Beam width is set to 50 to conform with the beam width of vanilla beam search decoding.

Train model

>python main.py --mode train --fast --data_dir path/to/iam  --batch_size 500 --early_stopping 15

