# Student Presentation Timer ⏳⏰🏃‍♂️🏃🏻‍♀️

The Student Presentation Timer is a simple HTML/JS countdown timer designed specifically for universities to monitor student presentations and ensure every student gets an equal speaking time, featuring features like color scheme change, distinct beep sounds, and a customizable countdown period.

![Image of timer paused at 00:31](https://raw.githubusercontent.com/newzealandpaul/StudentPresentationTimer/cd92a4c55258a6c67830f1877631edae9e22df77/screenshots/paused.png)

## Description

The timer application counts down in an MM:SS (e.g., 10:00) format from a time specified by the user. It has been incorporated with several features to encourage students not to exceed their allocated time:

- It visually alerts users by switching the color scheme to a flashing red and black when only 30 seconds are remaining (default setting).
- A single beep is activated when there are only 10 seconds left.
- A double beep sounds every 10 seconds by default from 00:00 onwards.
- It continues to count down past zero into 'negative' time to show how much over the time limit the presenter has gone.

By default, it starts making a beep sound when there are 10 seconds left.

The countdown defaults can be adjusted either by editing the source file or by appending a time query parameter, for example  `?time=10:00`, to the URL.

## Limitations & Caveats 

- The maximum countdown limit is 59:59 (59 minutes and 59 seconds).
- It is optimized for Chromium-based browsers (Google Chrome, Microsoft Edge, and Brave) and Firefox. It also works on desktop Safari but on occasion, the beeping does not function.
- For mobile devices, it works optimally in landscape orientation. However, for iOS devices, the audio beeping functionality does not work.
- It loads three external Javascript dependencies from the [unpkg.com](https://unpkg.com) content delivery network.

## Online Demonstration & Tool Usage

If you don't want to host this application yourself, you can use the [demo](https://steady-wisp-fe3562.netlify.app/timer.html?time=10:00). This timer defaults to 10:00 minutes. You can adjust the timer by changing the URL.

## Development and Testing

For development purposes, the query parameter `tick` allows you to adjust the tick rate in milliseconds. For example, [timer.html?time=10:00&tick=100](https://steady-wisp-fe3562.netlify.app/timer.html?time=10:00&tick=100) will take 1 minute of real-time to count down 10 minutes. This is useful for testing when making modifications to your timer. The application attempts to speed up the playback of the beep with mixed results.

## Acknowledgments

Special thanks to James Williams for the original idea and default timing setup.