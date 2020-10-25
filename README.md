# BERT NER
Use google BERT to do NER task

## Requirements

- python3
- pytorch>=1.2.0
- transformers=2.5.1
- pip3 install -r requirements.txt

## Run

python run_ner.py --data_dir=./data --bert_model=bert-base-cased --task_name=ner --output_dir=out_base --max_seq_length=128 --do_train --num_train_epochs=5 --do_eval --warmup_proportion=0.1

## Data Format

Using `-DOCSTART` as the identifier for each separate file, and the format of train data is that the first part of each line must be the token and the last part must be the label. In NER task, the label scheme can be BIO,  BIOES or other scheme, which need to be set in`def get_label()` function. The example train data is CoNLL-2003, and each line contains: `word POS Label`, separated by space. You can use your own data by imitating the format of example data, more simpler you can exclude the POS tag. 

