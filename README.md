# qcobjects-demo-effects

Here are some examples of how to use high-level effects in QCObjects.

Check out this live demo [here](https://qcobjects.github.io/qcobjects-demo-effects/) to see how to use the effects in a simple example.

Check out this project on GitHub [here](https://github.com/QCObjects/qcobjects-demo-effects)

# FadeIn

```javascript
function applyFadeIn (element) {
                    Fade.apply(element, 0, 1);
                }
```

# FadeOut

```javascript
function applyFadeOut (element) {
                    Fade.apply(element, 1, 0);
                }
```

# Move

```javascript
function applyMove (element) {
                    Move.apply(element, 0, 0, 100, 100);
                    setTimeout(() => {
                        Move.apply(element, 100, 100, 0, 0);
                    }, 1000);
                }
```

# Resize

```javascript
function applyResize (element) {
                    Resize.apply(element, 0, 1);
                }
```

# Radius

```javascript
function applyRadius (element) {
                    let element2 = global.get("mainControllerInstance")
                    .component.shadowRoot.subelements(".panel").pop();

                    let element3 = global.get("mainControllerInstance")
                    .component.shadowRoot.subelements("button")
                    .map(e => Radius.apply(e, 0, 27));

                    Radius.apply(element2, 0, 27);
                }
```

# WipeLeft

```javascript
function applyWipeLeft (element) {
                    WipeLeft.apply(element, 0, 1);
                }
```

# WipeRight

```javascript
function applyWipeRight (element) {
                    WipeRight.apply(element, 0, 1);
                }
```

# WipeUp

```javascript
function applyWipeUp (element) {
                    WipeUp.apply(element, 0, 1);
                }
```

# WipeDown

```javascript
function applyWipeDown (element) {
                    WipeDown.apply(element, 0, 1);
                }
```

# Rotate

```javascript
function applyRotate (element) {
                    element.style.transformOrigin = "center center";
                    Rotate.apply(element, 0, 360);
                }
```

# RotateX

```javascript
function applyRotateX (element) {
                    element.style.transformOrigin = "center center";
                    RotateX.apply(element, 0, 360);
                }
```

# RotateY

```javascript
function applyRotateY (element) {
                    element.style.transformOrigin = "center center";
                    RotateY.apply(element, 0, 360);
                }
```

# RotateZ

```javascript
function applyRotateZ (element) {
                    element.style.transformOrigin = "center center";
                    RotateZ.apply(element, 0, 360);
                }
```

# SlideInLeft

```javascript
function applySlideInLeft (element) {
                    Move.apply(element, -element.clientWidth, 0, 0, 0);
                }
```

# SlideInRight

```javascript
function applySlideInRight (element) {
                    Move.apply(element, element.clientWidth, 0, 0, 0);
               }
```

# FallFromTop

```javascript
function applyFallFromTop (element) {
                    Move.apply(element, 0, -element.clientHeight, 0, 0);
                }
```

# RiseFromBottom

```javascript
function applyRiseFromBottom (element) {
                    Move.apply(element, 0, element.clientHeight, 0, 0);
                }
```