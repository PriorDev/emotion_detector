import unittest

from emotion_detection import emotion_detector

class TestJoy(unittest.TestCase):
    def test1(self):
        response = emotion_detector("I am glad this happened")
        self.assertEqual(response['dominant_emotion'], "joy")

class TestAnger(unittest.TestCase):
    def test1(self):
        response = emotion_detector("I am really mad about this")
        self.assertEqual(response['dominant_emotion'], "anger")

class TestDisgust(unittest.TestCase):
    def test1(self):
        response = emotion_detector("I feel disgusted just hearing about this")
        self.assertEqual(response['dominant_emotion'], "disgust")

class TestSad(unittest.TestCase):
    def test1(self):
        response = emotion_detector("I am so sad about this")
        self.assertEqual(response['dominant_emotion'], "sadness")

class TestFear(unittest.TestCase):
    def test1(self):
        response = emotion_detector("I am really afraid that this will happen")
        self.assertEqual(response['dominant_emotion'], "fear")



if __name__ == '__main__':
    unittest.main()