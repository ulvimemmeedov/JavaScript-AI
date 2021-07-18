# JavaScript-AI
### What is JavaScript?
JavaScript is the Programming Language for the Web.
JavaScript can update and change both HTML and CSS.
JavaScript can calculate, manipulate and validate data. (W3 Shcool)

### What is NodeJs?
As an asynchronous event-driven JavaScript runtime, Node.js is designed to build scalable network applications. In the following "hello world" example, many connections can be handled concurrently. Upon each connection, the callback is fired, but if there is no work to be done, Node.js will sleep.(nodejs.org)
#### Example
```javascript
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

### What is TensorFlow.js ?

TensorFlow.js is a library for machine learning in JavaScript
Develop ML models in JavaScript, and use ML directly in the browser or in Node.js.

### What is Ai
Artificial intelligence (AI) is intelligence demonstrated by machines, as opposed to the natural intelligence displayed by humans or animals. Leading AI textbooks define the field as the study of "intelligent agents": any system that perceives its environment and takes actions that maximize its chance of achieving its goals. Some popular accounts use the term "artificial intelligence" to describe machines that mimic "cognitive" functions that humans associate with the human mind, such as "learning" and "problem solving"(wikipedia)

### Used Modules

 - [ @tensorflow/tfjs (Github)](https://github.com/tensorflow/tfjs)
 - [ @tensorflow-models/posenet (npm)](https://www.npmjs.com/package/@tensorflow-models/posenet)
 - [ translate.google.com (w3 School)](https://www.w3schools.com/howto/howto_google_translate.asp)


 ### Installation

#### install Tensorflow.js

 ```terminal
npm install @tensorflow/tfjs
```
or

##### CDN

 ```html
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs"></script>
```

#### install posenet.js

 ```terminal
npm install @tensorflow-models/posenet
```
or

##### CDN

 ```html
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow-models/posenet"></script>
```
#### google translate
 ```html
    <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
```

 ### Example posenet
 
 ```javascript
    posenet.load().then(function (net) {
        
        const pose = net.estimateSinglePose(image, {

            flipHorizontal: false,
            maxDetections: 2,
            scoreThreshold: 0.6,
            nmsRadius: 20

        });
    
        return pose;

    }).then((pose) => {

        console.log(pose);
        
    })
```
##### output
```output
{score: 0.011492787832942079, keypoints: Array(17)}keypoints: Array(17)0: part: "nose"position: {x: 1027.842830732175, y: 278.6836850652435}score: 0.01063799113035202__proto__: Object1: {score: 0.013458100147545338, part: "leftEye", position: {…}}2: {score: 0.015748053789138794, part: "rightEye", position: {…}}3: {score: 0.003821148071438074, part: "leftEar", position: {…}}4: {score: 0.020616019144654274, part: "rightEar", position: {…}}5: {score: 0.009801343083381653, part: "leftShoulder", position: {…}}6: {score: 0.011468672193586826, part: "rightShoulder", position: {…}}7: {score: 0.00891879852861166, part: "leftElbow", position: {…}}8: {score: 0.010363047011196613, part: "rightElbow", position: {…}}9: {score: 0.014903021976351738, part: "leftWrist", position: {…}}10: {score: 0.013811379671096802, part: "rightWrist", position: {…}}11: {score: 0.016689257696270943, part: "leftHip", position: {…}}12: {score: 0.01990378648042679, part: "rightHip", position: {…}}13: {score: 0.006293421145528555, part: "leftKnee", position: {…}}14: {score: 0.008604282513260841, part: "rightKnee", position: {…}}15: {score: 0.004809189587831497, part: "leftAnkle", position: {…}}16: {score: 0.005529880989342928, part: "rightAnkle", position: {…}}length: 17__proto__: Array(0)score: 0.011492787832942079__proto__: Object

```
##### image
![alt text](https://github.com/ulvimemmeedov/JavaScript-AI/blob/master/Example.png)

