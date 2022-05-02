# LibriSpeech ASR with seq2seq models (CTC + attention).
This folder contains the scripts to train a seq2seq system using LibriSpeech (10 hrs).
You can download LibriSpeech at https://dl.fbaipublicfiles.com/librilight/data/librispeech_finetuning.tgz
and find the instruction about the data at https://github.com/facebookresearch/libri-light/blob/main/data_preparation/README.md#2-get-the-limited-supervision-train-data
The csv files can be donwloaded [here](https://home.ttic.edu/~jcchou/course_files/csvs.zip)

# How to run
python train.py hparams/file.yaml
Remember to specify the path of your data. For example: 
`python train_with_wav2vec.py hparams/train_with_wav2vec.yaml --data_folder YOUR_DATA_FOLDER --csv_folder YOUR_CSV_FOLDER --output_folder YOUR_OUTPUT_FOLDER --ctc_weight 0.0 --number_of_ctc_epochs 0 --freeze "True" --dec_neurons 256`

# Reference Results
dev-clean WER=22.26 <br>
dev-other WER=30.23 <br>

# Training Time
It takes about 10 minutes for each epoch on a NVDIA 2080 ti.

# **About SpeechBrain**
- Website: https://speechbrain.github.io/
- Code: https://github.com/speechbrain/speechbrain/
- HuggingFace: https://huggingface.co/speechbrain/


# **Citing SpeechBrain**
Please, cite SpeechBrain if you use it for your research or business.

```bibtex
@misc{speechbrain,
  title={{SpeechBrain}: A General-Purpose Speech Toolkit},
  author={Mirco Ravanelli and Titouan Parcollet and Peter Plantinga and Aku Rouhe and Samuele Cornell and Loren Lugosch and Cem Subakan and Nauman Dawalatabad and Abdelwahab Heba and Jianyuan Zhong and Ju-Chieh Chou and Sung-Lin Yeh and Szu-Wei Fu and Chien-Feng Liao and Elena Rastorgueva and François Grondin and William Aris and Hwidong Na and Yan Gao and Renato De Mori and Yoshua Bengio},
  year={2021},
  eprint={2106.04624},
  archivePrefix={arXiv},
  primaryClass={eess.AS},
  note={arXiv:2106.04624}
}
```
