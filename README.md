# Medical-Dialogue-Corpus
Here we deliver the medical dialogue corpus collected from online open source. These corpora will be used to fine-tune the entity prediction model and the dialogue generation model.
1. https://github.com/UCSD-AI4H/Medical-Dialogue-System 
2. https://github.com/Toyhom/Chinese-medical-dialogue-data 
3. https://github.com/flyyuan/Chinese-Medical-QA-Data 
4. https://github.com/liuhuanyong/MiningZhiDaoQACorpus
5. https://github.com/zhangsheng93/cMedQA2
6. https://github.com/lddsdu/VRBot


# Curriculum boost learning strategy
1. The original pre-trained model (i.e., BertGPT-Entity) is utilized to initialize the parameters of the
encoder and decoder, which is fine-tuned with the cleaned online medical dialogues. Then, we use
the boost strategy to train 4 epochs for a total of 5-fold;
2. The dialogues with entities of the doctor is used for training, so that the generated response will
contain the common features of doctors. We use the boost strategy to train 4 epochs for a total of
5-fold;
3. We further sort out the dialogues with entities of doctors, whose length is greater than 11 (counted
on the validation set) to train the dialogue generation model, because these dialogues have more
entity characteristics. It is easier for the model to adapt to generating longer sentences. We train
2 epochs for a total of 5-fold.

As for more information, feel free to email at libincn@hnu.edu.cn.
