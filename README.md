# -
情感音乐利用情感识别技术和机器学习算法,根据用户的实时情感状态和音乐偏好,推荐匹配的音乐,营造个性化的聆听体验。
import random

# Simulate emotion detection based on text input
# In a real-world application, this would involve natural language processing and perhaps sentiment analysis
def detect_emotion(input_text):
    emotions = ['happy', 'sad', 'angry', 'relaxed']
    return random.choice(emotions)  # Simulating emotion detection

# A simple recommendation system based on the detected emotion
# This would ideally be replaced with a machine learning model trained on user preferences and song attributes
def recommend_music(emotion):
    music_database = {
        'happy': ['Song A - Artist 1', 'Song B - Artist 2'],
        'sad': ['Song C - Artist 3', 'Song D - Artist 4'],
        'angry': ['Song E - Artist 5', 'Song F - Artist 6'],
        'relaxed': ['Song G - Artist 7', 'Song H - Artist 8']
    }
    
    if emotion in music_database:
        return random.choice(music_database[emotion])
    else:
        return "No recommendation available for this emotion."

# Main function to simulate the recommendation engine
def main():
    print("Welcome to Emotion Music!")
    user_input = input("How are you feeling today? ")
    detected_emotion = detect_emotion(user_input)
    print(f"Detected emotion: {detected_emotion}")
    recommended_song = recommend_music(detected_emotion)
    print(f"Recommended song for you: {recommended_song}")

if __name__ == "__main__":
    main()
