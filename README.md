# FineMuSe

This repository is associated with the research paper titled *Beyond Binary Classification: Detecting Fine-Grained Sexism in Social Media Videos*, Laura De Grazia, Danae Sánchez Villegas, Desmond Elliott, Mireia Farrús, and Mariona Taulé.

To advance research on fine-grained sexism detection, we present FineMuSe, a new fine-grained multimodal dataset for sexism detection in Spanish (European and Peninsular). FineMuSe includes videos from the MuSeD dataset, which originally contained only binary annotations for TikTok and BitChute videos. In FineMuSe, these videos have been extended with fine-grained annotations. Additionally, the dataset includes a new data source, YouTube Shorts, which contains both binary and fine-grained annotations. For convenience, we refer to the TikTok and BitChute videos as Part 1 (P1) and the YouTube Shorts videos as Part 2 (P2).

The final dataset contains 828 videos, each labeled as sexist or non-sexist, and includes granular annotations for both sexist and non-sexist content. The annotations were developed using a three-level hierarchical taxonomy, with the first level comprising mutually exclusive categories and the second and third levels comprising categories that may co-occur. 

<img width="749" height="261" alt="taxonomy_sexism" src="https://github.com/user-attachments/assets/23e3b7cf-c3b2-46a3-b25b-c6ab8dc68682" />

---


<h2>
  <img width="40" alt="analysing" src="https://github.com/user-attachments/assets/72d52d34-1889-447a-9928-71a698a710f9" />
  Dataset Statistics
</h2>

FineMuSe has a balanced distribution between sexist and non-sexist content, with 48.5% of the videos labeled as sexist in P1 and 54.2% in P2. The following figures illustrate the distribution of sexist and non-sexist categories across P1 and P2:

<div>
  <img width="424" height="280" alt="sexist_types" src="https://github.com/user-attachments/assets/7d664369-752a-44fc-af4e-0842330d5bb2" />
  <img width="424" height="280" alt="non_sexism" src="https://github.com/user-attachments/assets/eda755f4-29ea-40ca-bf28-aacb2528a78c" />
</div>

--- 

<h2>
  <img width="40" alt="check" src="https://github.com/user-attachments/assets/1763a843-f6ee-4322-9918-55e9629dca34" />
  Annotation Process
</h2>

We relied on six expert annotators of diverse genders and ages to ensure demographic variety. The group was split into two teams, each assigned half of the dataset. Annotation followed a three-step approach: first, annotating text transcripts; second, annotating audio; and finally, annotating videos. Each team annotated the text transcripts and video for their assigned subset, while the other team handled the audio. Inter-annotator agreement was higher for the binary annotation task than for the fine-grained task, highlighting the difficulty of the multi-label classification problem. For the video modality, agreement increased from substantial (0.61–0.80) for text to almost perfect (0.81–1.00) for audio. The following figures illustrate the Fleiss’ Kappa values for the fine-grained sexist categories across text and video modalities in P1 and P2.

<img width="719" height="234" alt="Screenshot 2026-02-05 at 15 08 27" src="https://github.com/user-attachments/assets/b0fee235-38d4-4092-a332-d0724f60887f" />

---
<h2>
  <img width="40" alt="robot" src="https://github.com/user-attachments/assets/1a1a55e2-93f3-440b-a683-d5dcfe134b54" />
  Evaluation of LLMs and Multimodal LLMs 
</h2>

We evaluated a wide range of LLMs that process text-only inputs as well as multimodal LLMs that integrate both text and images. The task first requires determining whether a social media post is sexist and, if so, identifying its specific type(s) of sexism. All evaluations were conducted against labels assigned by annotators who had access to the full video. The following figure illustrates the results for the fine-grained task, using Macro F1 as the evaluation metric, computed over all ground-truth sexist instances:


<img width="1138" height="424" alt="macro_f1" src="https://github.com/user-attachments/assets/676e150a-073e-4319-a79c-18900fa9b54d" />

