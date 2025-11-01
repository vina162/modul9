# 🔄 Flutter Fingerprint Counter App

A fun and interactive Flutter app featuring a *circular progress bar* that increases every time you tap the *fingerprint icon*.  
It demonstrates the use of *ValueNotifier*, *StatefulWidget*, and *simple_circular_progress_bar* package for dynamic UI updates.

---

## 🧩 Features

✅ Circular progress indicator that fills gradually  
✅ Tap-based counter using a *fingerprint icon*  
✅ Real-time progress updates with `ValueNotifier`  
✅ Floating action button to *reset progress*  
✅ Clean modern UI with `Material 3` design  

---

## 🧠 How It Works

1. The app initializes a counter (`counter = 0`) and a `ValueNotifier<double>` to control the progress bar value.  
2. Each tap on the *fingerprint icon* triggers the `incrementCounter()` function, adding 1 until reaching *33 taps* (100%).  
3. The `ValueNotifier` updates the progress bar in real-time.  
4. The `resetCounter()` function resets both counter and progress to 0.  

---

## ⚙️ Code Structure

```
lib/
├── main.dart              # Main app file with state management & UI
```

---

## 🧱 Widgets Breakdown

- *SimpleCircularProgressBar* → shows dynamic circular progress  
- *ValueNotifier* → notifies progress changes efficiently  
- *InkWell + Icon* → detects fingerprint taps  
- *FloatingActionButton* → resets the counter  
- *SystemChrome* → makes status bar transparent  

---

## 🖥️ UI Preview

```
---------------------------------------------
|             [Counter: 10]                 |
|                                           |
|          ⭕ Circular Progress ⭕           |
|                                           |
|         🔘 Fingerprint Button             |
|                                           |
|                🔄 Reset FAB               |
---------------------------------------------
```

---

## 🧰 Tech Used
- *Flutter SDK*
- *Dart Language*
- *simple_circular_progress_bar* package
- *Material Design 3*
- *ValueNotifier* for state management

---

## 💡 Example Code Snippet

```dart
void incrementCounter() {
  setState(() {
    if (counter < 33) {
      counter++;
      _valueNotifier.value = (counter / 33) * 100;
    }
  });
}
```

---

## 💬 Result Summary
This project beautifully combines animation, interactivity, and responsive design using Flutter.  
It’s a perfect example of *progress visualization* and *real-time UI updates* — simple yet engaging!

---

✨ *Built with Flutter — Fast, reactive, and fun to develop!*
