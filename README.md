# Neural Style Transfer of Live Video

<img src="https://imgur.com/pT3YfW8.gif"/>

---

## Webcam App

The `webcam-app` folder contains an app that uses OpenCV and runs on Mac and Linux. It loads one of two saved PyTorch models (`green_swirly.pth` or `candy.pth`). The app loads your webcam feed (which must be configured as `/dev/video0`), stylizes it, and displays the output. You should be able to quit by pressing `q`. Sometimes it is cranky and needs to be manually killed. In this case run:

```bash
APP=$(ps | awk '/webcam_app.py/ {print $1}')
kill -9 "$APP"
```

To switch between the models, edit line 12 of the `webcam_app.py` file to say either 

```python
weights_fname = "candy.pth"
```

or

```python
weights_fname = "green_swirly.pth"
```
