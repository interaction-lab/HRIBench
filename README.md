# HRIBench

To systematically study VLM capabilities in human perception for HRI and performance-latency trade-offs, we introduce HRIBench, a visual question-answering (VQA) benchmark designed to evaluate VLMs across a diverse set of human perceptual tasks critical for HRI. HRIBench covers five key domains: (1) non-verbal cue understanding, (2) verbal instruction understanding, (3) human-robot-object relationship understanding, (4) social navigation, and (5) person identification. To construct HRIBench, we collected data from real-world HRI environments to curate questions for non-verbal cue understanding, and leveraged publicly available datasets for the remaining four domains. We curated 200 VQA questions for each domain, resulting in a total of 1000 questions for HRIBench.

You can find more details regarding our methods and results in [our paper](https://arxiv.org/abs/2506.20566).

### Dataset Access

You can download HRIBench using [this google drive link](https://drive.google.com/drive/folders/1nb0iFCXC9FiMFV9sUWzfjW7owm2Dlmmo?usp=sharing).

Currently, the following four domains are publicly available in the google drive above: (1) non-verbal cue understanding (Non_Verbal), (2) verbal instruction understanding (Ins_Follow), (3) human-robot-object relationship understanding (HROI), (4) social navigation (Social_Nav).

Since we used frames from YouTube videos for the domain of person identification (Id_Rec), we are still looking into rules regarding copyright before publicly releasing data for this domain.

### Dataset Structure

HRIBench follows the same dataset strcture as [ManipBench](https://arxiv.org/pdf/2505.09698).

For each domain, there are 200 VQA questions (demo_0 - demo_199). Within each question, the following files are included:

- driod.txt: This file includes the question prompt with the options.
- correct_answer.json: This file includes the correct answer.
- wrong_answers/wrong_answers.json: This file include the wrong answers.
- wrong_answers/processed_frame.png: This file include the input image with all the visual options for the VQA questions.
- wrong_answers/processed_frame.png: Only questions in the Id_Rec domain includes this file, which is the photo of the person VLM needs to identify from the available options.

### Results Logs

You can find our results logs saved as JSON files in their corresponding directories in this repo.

### Citation

```bibtex
@article{shi2025hribench,
  title={HRIBench: Benchmarking Vision-Language Models for Real-Time Human Perception in Human-Robot Interaction},
  author={Shi, Zhonghao and Zhao, Enyu and Dennler, Nathaniel and Wang, Jingzhen and Xu, Xinyang and Shrestha, Kaleen and Fu, Mengxue and Seita, Daniel and Matari{\'c}, Maja},
  journal={19th International Symposium on Experimental Robotics (ISER)},
  year={2025}
}
```
