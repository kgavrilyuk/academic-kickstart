+++
title = "Actor and Action Video Segmentation from a Sentence"
date = "2018-03-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["K. Gavrilyuk", "A. Ghodrati", "Z. Li", "C. G.M. Snoek"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "in *Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition*, Salt Lake City, USA, 2018."
publication_short = "*CVPR*"

# Abstract and optional shortened version.
abstract = "This paper strives for pixel-level segmentation of actors and their actions in video content. Different from existing works, which all learn to segment from a fixed vocabulary of actor and action pairs, we infer the segmentation from a natural language input sentence. This allows to distinguish between fine-grained actors in the same super-category, identify actor and action instances, and segment pairs that are outside of the actor and action vocabulary. We propose a fully-convolutional model for pixel-level actor and action segmentation using an encoder-decoder architecture optimized for video. To show the potential of actor and action video segmentation from a sentence, we extend two popular actor and action datasets with more than 7,500 natural language descriptions. Experiments demonstrate the quality of the sentence-guided segmentations, the generalization ability of our model, and its advantage for traditional actor and action segmentation compared to the state-of-the-art."

# Featured image thumbnail (optional)
image_preview = "actor_action.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/#project/`.
# projects = [""]

# Links (optional).
url_pdf = "http://openaccess.thecvf.com/content_cvpr_2018/papers/Gavrilyuk_Actor_and_Action_CVPR_2018_paper.pdf"
url_preprint = ""
# url_code = "#"
# url_dataset = "#"
url_project = ""
# url_slides = "#"
url_video = ""
# url_poster = "#"
url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{name = "arXiv", url = "https://arxiv.org/abs/1803.07485"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
image = "actor_action.png"
caption = ""

+++

## Datasets
### A2D Sentences
We have extended [Actor and Action (A2D) Dataset](https://web.eecs.umich.edu/~jjcorso/r/a2d/) with additional description of every object is doing in the videos. We provide three files containing our annotation:

1. [a2d_annotation.txt](/actor_action/a2d_annotation.txt) contains annotation in the format "video_id,instance_id,query" where:

	* "video_id" - the original id of the video from the A2D dataset

	* "instance_id" - the id of the object in the video that we have added to the original annotation

	* "query" - the description of what object is doing throughout the whole video (see the paper for more details)

2. [a2d_annotation_with_instances.zip](https://drive.google.com/file/d/14DNamenZsvZnb32NFBNkZCGene5D2oaE/view) - the original annotation from the A2D dataset in HDF5 with the field "instance" added. This field corresponds to "instance_id" field in the *a2d_annotation.txt* file. 

3. [a2d_missed_videos.txt](/actor_action/a2d_missed_videos.txt) contains all the videos that were not annotated with descriptions and therefore were excluded from experiments in the paper. 

### J-HMDB Sentences
We have extended [J-HMDB Dataset](http://jhmdb.is.tue.mpg.de/) with additional description of every human is doing in the videos:

1. [jhmdb_annotation.txt](/actor_action/jhmdb_annotation.txt) contains annotation in the format "video_id,query":

	* "video_id" - the original id of the video from the J-HMDB dataset
	
	* "query" - the description of what human is doing throughout the whole video (see the paper for more details)

