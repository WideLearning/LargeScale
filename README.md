# LargeScale
Learning how to pre-train big transformers.

## Running
First unpack the dataset:
```
zstd -d dataset.tar.zstd && tar -xf dataset.tar && rm dataset.tar
```

Check that `transformers`, `datasets`, `evaluate` and other libraries are of latest versions.

Now, run the training script with the right settings. For example, the laptop-friendly one:
```
python3 hf.py --model_type gpt2 --train_file train.txt --validation_file eval.txt --output_dir output --tokenizer gpt2 --do_train True --config_overrides="n_layer=2,n_embd=120"
```
