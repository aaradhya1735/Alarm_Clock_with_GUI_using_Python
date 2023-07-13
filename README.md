# Alarm_Clock_with_GUI_using_Python
Alarm Clock with GUI Using Python with specific buttons for snooze and stop.

The provided code is an implementation of an alarm clock GUI using tkinter in Python. It allows users to set an alarm by entering the desired time, plays an alarm sound when the set time is reached, and provides options to stop the alarm or snooze it.

Here's a breakdown of the code:

1. The necessary libraries are imported: tkinter for GUI, messagebox for displaying messages, threading for handling the alarm in a separate thread, time for time-related operations, pygame.mixer for playing audio, and PIL for working with images.

2. The `alarm` function is defined, which retrieves the alarm time entered by the user, checks if it's empty, and starts a separate thread to wait for the alarm time and play the alarm sound.

3. The `wait_and_play` function is defined, which runs in a separate thread and waits until the alarm time is reached. Once the time matches, it calls the `play_music` function to play the alarm sound.

4. The `play_music` function initializes the mixer, loads the alarm sound file, and plays it using `mixer.music.play`. It also enables the Stop and Snooze buttons.

5. The `stop_alarm` function stops the alarm sound using `mixer.music.stop` and disables the Stop and Snooze buttons.

6. The `snooze_alarm` function snoozes the alarm for a fixed duration (here, 60 seconds) by using `time.sleep` and then calls the `play_music` function to restart the alarm sound.

7. The `update_time` function is defined to update the time label with the current time using `time.strftime`. It is called every second using `root.after` to continuously update the displayed time.

8. The GUI window is created using `Tk()`, and its title and dimensions are set.

9. The canvas is created to display an image using `Canvas` and `create_image`. The image is loaded using `Image.open` from PIL and converted to ImageTk format using `ImageTk.PhotoImage`. The canvas is then packed to display it in the GUI.

10. Frames are created for the header, input box, and buttons using `Frame`. The header frame has a custom background color, and the other frames are positioned using `place`.

11. The user input field for entering the alarm time is created using `Entry`.

12. The Set Alarm button is created using `Button` and linked to the `alarm` function.

13. The Stop and Snooze buttons are created using `Button` and linked to the `stop_alarm` and `snooze_alarm` functions respectively. Initially, both buttons are disabled using `state=DISABLED`.

14. A label is created to display the current time using `Label`.

15. The header frame is packed using `fill=X` to extend it horizontally.

16. The `update_time` function is called to start updating the time label.

17. Finally, the GUI main loop is started using `root.mainloop()`.

To run this code, you need to have the necessary libraries installed (tkinter, pygame, PIL) and provide suitable image and audio files ("download.png" and "ALM.mp3" respectively) in the same directory as the Python script.
