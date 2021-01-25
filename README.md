# The Microsoft Research Paraphrase Corpus (MRPC) Dataset

MRPC is a dataset (also an NLP task) that contains 5800 pairs of 
sentences extracted from news sources on the web, along with human
annotations indicating each sentence pair captures a paraphrase or
semantic equivalence relationship. The dataset is published on
Jan 3rd 2005.

The paper is uploaded in this repo named `MRPC_2005.pdf`.

Note: According to the paper, there should be 5800 sentence pairs in
the dataset. However, as we found in the dataset file, there is
5801 sentence pairs. Therefore, we record this issue here in case
that some users find out by themselves and feel strange.

MRPC is also included a task in the General Language Understanding Evaluation
(GLUE). Due to the copyright issue, GLUE can only provide a pre-processing
routine to reorganize MRPC dataset, rather than include the original dataset
in it, or directly publicize the reorganized dataset. Therefore, users
need to complete two steps to use the MRPC dataset in their DL models.

1. Download the raw dataset from Microsoft and unzip the file. This is
what code in this repo is doing.

2. Pre-processing the dataset using script from GLUE. Details of this step
is shown in GLUE's repo.

# Download and Unzip MRPC Dataset

The steps to download and unzip MRPC dataset.

1. Run `download_mrpc.zsh` to download.

2. Wait! Actually the unzipped files are committed in this repo. You can
just skip next step and continue.

3. Run `process_mrpc.zsh` to unzip and complete other minor operations.

The output of the processing are two txt files

1. `./MRPC/msr_paraphrase_test.txt`
2. `./MRPC/msr_paraphrase_train.txt`

Both files are less than 1MB in size, so these two files are
committed to github as well. The user does not need to run
the two steps above in order to use the MRPC dataset.

`msr_paraphrase_test.txt` contains 1725 entries of sentences pairs with
labeling and IDs.

`msr_paraphrase_train.txt` contains 4076 entries of sentences pairs with
labeling and IDs

The test and train set has 5801 pairs add up together.

