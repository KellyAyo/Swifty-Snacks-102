<h2>Swifty Snacks 102: Can’t you see?</h2>

Adding new UIView based elements to view controllers, is fairly intuitive when using storyboards.

Given that Swifty Snacks ‘don’t use no damn storyboards’, you might be wondering how best to add UIView based elements to view controllers programmatically.

Typically, we use a 3- step procedure. Firstly, we ‘flesh-out’ the particulars for our new element inside an executable block. We then add the element, as a subview of our viewcontroller’s ‘view.’ Lastly, inside a dedicated function we position the new element within it’s superview i.e. the viewcontroller’s view.

Let us begin by sketching the design pattern, described above, in code.

<img src="Swifty Snacks 102/image1.png">

Part 1 shows the executable block, to be used when detailing our new element. We will proceed to add this element as a subview to our viewcontroller’s view in Part 2 — viewDidLoad(). Additionally, we will invoke Part 3, from viewDidLoad(), using the setupTestView() function. In Part 3 we will conclude by specifying the position of our testView, using autolayout contraints.

Let’s build out Part 1. Start by setting an instance of UIView to the ‘tV’ keyword. Next, to distinguish the new element from it’s superviews background, set tV’s background colour to red. Next, in order to allow Auto Layout to dynamically calculate the size and position of our new view, we must set tV’s translatesAutoresizingMaskIntoConstraints property to equal false. End by returning our instance of tV. Note that the () following the closing brace executes the block.

<img src="Swifty Snacks 102/image2.png">

In Part 2, first set our viewcontroller’s backgroundColor to white. Proceed to add the new testView as a subview of the viewcontroller’s view. Lastly, call setupTestView(), to size and position testView within our viewcontroller’s view.

To close, in Part 3, employ Auto Layout constraints to position testView within it’s superview. Note: it is necessary to set each of the constraints to isActive = true.

<img src="Swifty Snacks 102/image3.png">

“Two is one and one is none” — US Navy Seals

