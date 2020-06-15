This Blazor project is a demonstration of how onkeypress does not seem to work in the Edge browser.

Steps to reproduce the issue:

1. run the project
2. click on the button to set focus
3. press keys

Expected output:

Each key press should display on screen.

Actual output:

No key presses are detected/displayed.

Works fine in Chrome and Firefox.

Fails in Microsoft Edge 44.18252.1000.0

Bug report:

### Functional impact
Code that is reliant on using onkeypress will not work.

### Minimal repro steps
Sample project: https://github.com/SQL-MisterMagoo/BlazorBug/tree/master/BlazorEdgeBug

1. Create a new Blazor project
2. Add a button and hook up onkeypress to it
3. in your onkeypress handler, assign args.Code to a field on the page
4. add your field to the page inside a span (e.g.)
5. Run the project
6. Click on the button with the onkeypress event handler
7. Type anything - on edge it will not pick up the key presses

### Expected result
Each key press should fire the associated onkeypress event.

### Actual result
The event does not fire.

### Further technical details
Microsoft Edge 44.18252.1000.0
Works in Chrome 