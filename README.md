# FashionAssist
Architecture of the RecommendApparel.ipynb
![image](https://github.com/vkrisvasan/FashionAssist/assets/10602190/866cebf8-24a9-476c-a13c-0a3e95168ef1)

Flow of code
1. pass the URL of the Image or the Image from a file location and call find_similar_items method
2. call get_image method which gets the URL of the Image or the Image file and returns the vertexai vision_model Image Object
3. call get_img_embeddings with the Image object and the prompt as a text
4. call gemini model.get_embeddings to get get the vector embedding based on the Image Object and Prompt and return the embeddings 
5. call astra collection.vector_find with the emeddings and return the top 3 matched embedings as documents from the astra vector collection
6. call show_recommendations and print the 3 results
