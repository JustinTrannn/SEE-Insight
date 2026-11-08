# Notes

## 1/20/2026
Going to be talking about projects the next few weeks. These are some of the image segmentation projects that will be happening:
- Polymer residue detection: Detect polymer residues in paper sample images. 
- Broccoli: Detecting heads of broccoli.
- Cracks: Develop a semantic segmentation system to identify and distinguish the umbra and penumbra region of D-cracking.
- Tar Spots - Develop a small format app that can diagnose, detect and count "tar spots" on corn lear images. Integrate this tool into an app that can be used by farmers to track the spread of the disease.
- Cow Segmentation: Develop an automated computer vision system to track individual cattle and monitor nose-to-nose contact patterns for respitory disease survellience
LandGraph is taking multiple models and having them work together and compete against each other. LandGraph does much better with non-fine-tuned models than a fine-tuned model.

## 1/27/2026
Miriam, PhD student, is talking about LLM projects
- Relationship Classification: Useful for tasks such as information retrieval, knowledge graphs, question graphs, question-answering systems, understanding understanding and summarization of large text
- Fuzzy Cognitive Maps (FCM) Extraction and Evaluation: Manual labeling is expansive, data is too large. The solution is use LLMs instead.
- Feedback Generation for Essays: Automated essay scoring systems. Generate feedback using LLMs
- LLM Interpretability and Trust: Methods to understand what information a model uses, why it produces an output, and when it's likely to fail. It's not binary. It depends on task risk, data domain, and controls around use.
- Non-Traditional Active Learning: Training LLMs is resource intensive. Active learning reduces annotation effort by picking the most informative samples. Classic methods are uncertainty, diverstiy, model disagreement, ect.
- Noisy Labels, Weak/Self Supervision: A model that trains itself with no labels. Add label confidence/quality to loss function as new dimention.
- Legal Document Summarization: Summarize legal documents because they are very long. Summarize module, revision and judging module, long term memory store.
- Unsupervised Learning / Clustering: Apply natural language text embeddings to improve interpretability of textual data representations.

## 2/3/2026
- Come up with a uuraf thing to show to Dr. Colbry
- Talk about your project in it
- Send it to Dr. Colbry

## 2/24/2026
- Guest speaker: Dr. Rodriguez
- DRIVE lab - research focus areas
### Project 1: Early identification of HPAI in cows during outbreaks in robotic milking systems
- High pathogenic avian influenza (HPAI) is a zoonotic disease
- About 300,000 observations
- We also have infection status of cows during the outbreak
- Data in videos and ~20% already in Excel format using a numbers recognition software
- Taking data from milking cows to see if they are getting sick or are sick. That way they can be seperated from the rest of the cows
### Project 2: Predict ketosis postpartum based on metabolic parameters measure prepartum
- Ketosis is a metabolic disease affecting dairy cows
- Dataset of 120 cows measures 5 times each, with 16 metabolites per time point
- The objective is to predict detosis

## 3/10/2026
- Mihar finished the paper polymers
- Pipline steps: Image loading, hough transform (remove BG), CLAHE (equalize lighting), thresholding and measurement, convert area_px to area_mm^2
- He said he did not use PyTorch or TensorFlow. No neural networks used. He used OpenCV and Dr. Colbry said that a heuristic based approach and classical results.
- Cache is the compromise between NN, which he says you won't know what they're doing, because you can interpret it

## 3/24/2026
- Maryam got published
- People are giving updates on their subgroups

## 3/31/2026
- Kanban. Used a lot in industry. To help with organization of projects?
- People giving updates on their projects
- Next week, we will discuss when these meetings will be next semester

## 4/7/2026
- VIP discussion on April 14th 12:30-2:30pm. Dr. Colbry is trying to get faculty to try this VIP setup for next year

## 9/15/2026
- Week 3 of this class
- I'm in a project this year and it's "Automatic Plate Segmentation and Colony Feature Extraction"
- The goal is to count the number of colonies in a petri dish. Within the petri dish, it will be segmented into four parts. Each part has its own group of bacteria.
- I am currently reading some papers that Aadhya sent me
- After reading the articles, I think this will be difficult to achieve. There's a lot of methods that I haven't heard of such as watershed segmentation and using local minima based stuff. - They've already come up with a counter called CFUCounter and it did pretty well. Not sure if that's possible for to create something better than that but I'm sure it's possible.
- Article: Machine learning for enumeration of cell colony forming units by Louis Zhang

## 10/5/2026
- Started exploring ways to extract useful insights from the bacteriology dataset.
- Noticed that the structured dataset is relatively small, which could make it difficult to find meaningful trends or draw reliable conclusions.
- Considered using Python libraries such as Pandas, NumPy, and Matplotlib to analyze and visualize the data.
- Asked ChatGPT for help developing a template for approaching the project. I wanted a general pipeline that would help me organize the work instead of immediately jumping into coding.
- Began considering how to structure the workflow, starting with data exploration and eventually moving toward image segmentation and bacterial colony analysis.
- The biggest issue this week was figuring out how to extract useful insights from a small dataset. With limited observations, it is difficult to tell whether a pattern is meaningful or - just caused by random variation.
- I realized that traditional data analysis might not be the most useful starting point for this project, especially if there isn't enough structured information to analyze.
- Creating a pipeline helped me better understand how the different tasks relate to each other. Rather than immediately building a machine learning model, I could first focus on understanding the images and identifying the individual Petri dishes.
- Using ChatGPT as a planning resource was useful because it gave me a more organized way to approach a project that initially seemed overwhelming.

## 10/12/2026
- Continued following the project pipeline developed during the previous week.
- Focused on the data analysis stage to determine what information could realistically be extracted from the dataset.
- Concluded that it would be difficult to conduct meaningful statistical analysis because the structured dataset contains a limited number of observations.
- Began reconsidering the approach to the project. Instead of focusing heavily on finding patterns in the existing data, I started thinking about how image processing could be used to generate additional useful measurements.
- Identified image segmentation as an important step because isolating Petri dishes would make it easier to analyze their contents later.
- This week helped me realize that not every dataset is suitable for statistical analysis. Even if I can create graphs or calculate statistics, the results might not be very meaningful with such a small sample.
- I initially thought that the data analysis stage would provide more useful insights, but I realized that this approach had limitations.
- I learned that a project pipeline needs to be flexible. Sometimes an initial approach doesn't work as expected, and it's important to adjust based on what the data actually supports.

## 10/19/2026
- Decided to focus this week's work on segmenting a single Petri dish from an image.
- Planned to use some of the example code that Dr. Dirk shared the previous week as a possible starting point.
- Identified a few important tasks for this stage, including detecting the Petri dish, separating it from the background, and isolating the region that contains bacterial growth.
- Started thinking about how a successful segmentation step could lead to later analysis, such as separating the dish into quadrants and identifying bacterial colonies.
- I think focusing on one image first is a more manageable approach because it allows me to test individual steps without worrying about the entire dataset.
- One challenge I anticipate is accurately detecting the edges of the Petri dish, especially if the lighting, background, or positioning varies between images.
- The coding examples from Dr. Dirk seem like they could be a helpful starting point because I can build on existing techniques instead of trying to create everything from scratch.
- My main priority is to get a basic segmentation method working before moving on to more complicated tasks such as colony detection and counting.
- I also want to make sure the solution can eventually be applied to many images rather than only working on a single example.

## 10/30/2026
- Continued working on the image segmentation pipeline for the Petri dish project.
- Started creating a Jupyter Notebook that would take an image of a Petri dish and segment it from the background.
- Used Python libraries such as OpenCV, NumPy, and Matplotlib to process and visualize the images.
- Followed some of the image segmentation techniques from the notebook that Dr. Dirk shared with us.
- Started by loading an image and converting it from BGR to RGB and HSV to better understand the different color channels.
- Used HSV thresholding to identify the red agar in the Petri dish and create a binary mask that separates it from the background.
- Learned about morphological operations such as opening and closing. These operations help remove noise and fill small gaps in the binary mask.
- Used OpenCV's findContours function to detect the boundaries of objects in the image and selected the largest contour, assuming it represented the Petri dish.
- Applied fitEllipse to create a smoother outline around the detected Petri dish. This seemed useful because the dish might not appear perfectly circular depending on the camera angle.
- Created another binary mask using the fitted ellipse and used bitwise_and to remove everything outside the Petri dish.
- Ran into an error with bitwise_and because of the data type of the mask. I learned that OpenCV requires the mask to be an 8-bit image, so I had to make sure it was using uint8.
- I spent a lot of time this week trying to understand what each OpenCV function was actually doing instead of just copying the code.
- Some of the concepts were confusing at first, especially kernels, morphological operations, and how contours are represented as coordinates.
- I think I have a better understanding of how image segmentation works now. Instead of detecting the Petri dish directly, I'm using several image processing techniques to gradually isolate it from the background.
- My next step is to test the segmentation pipeline on more images and eventually divide each Petri dish into four quadrants.
- One concern I still have is whether the HSV thresholds and other parameters will work consistently across images with different lighting and backgrounds.

## 11/8/2026
- Decided to crop the final image of the petri dish.
- Created a new folder in the data folder called raw. It's made specifically for the raw images
- Created a new folder in the data folder called segmented. It's made for the segmented petri dishes
- Coded the segmented petri dish images to automatically save to the segmented folder
