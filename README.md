# UGUI的弹框实现

# Example
```cs
    public void Test()
    {
        MessageBox.Show("This is a message");
    }

    public void TestWithTitle()
    {
        MessageBox.Show("This is a message with a title.", "Message Box Title");
    }

    public void TestWithCallback()
    {
        MessageBox.Show(
            "This is a message with a callback.",
            "Message Box Callback Example",
            (result) => { MessageBox.Show("You Clicked " + result.ToString(), "Dialog Result"); }
        );
    }

    public void TestOKCancelButtons()
    {
        MessageBox.Show
        (
            "Are you sure you wish to delete your save game?",
            "Delete Save",
            (result) => { MessageBox.Show("You Clicked " + result.ToString(), "Dialog Result"); },
            MessageBoxButtons.OKCancel
        );
    }

    public void TestRetryCancelButtons()
    {
        MessageBox.Show
        (
            "This is a message with a set of buttons selected.",
            "Message Box Buttons Example",
            (result) => { MessageBox.Show("You Clicked " + result.ToString(), "Dialog Result"); },
            MessageBoxButtons.RetryCancel
        );
    }

    public void TestYesNoButtons()
    {
        MessageBox.Show
        (
            "Give us five stars?",
            "Review Game",
            (result) => { MessageBox.Show("You Clicked " + result.ToString(), "Dialog Result"); },
            MessageBoxButtons.YesNo
        );
    }

    public void TestYesNoCancelButtons()
    {
        MessageBox.Show
        (
            "This is a message with a set of buttons selected.",
            "Message Box Buttons Example",
            (result) => { MessageBox.Show("You Clicked " + result.ToString(), "Dialog Result"); },
            MessageBoxButtons.YesNoCancel
        );
    }

    public void TestAbortRetryIgnoreButtons()
    {
        MessageBox.Show
        (
            "Not ready reading drive A",
            "Message Box Buttons Example",
            (result) => { MessageBox.Show("You Clicked " + result.ToString(), "Dialog Result"); },
            MessageBoxButtons.AbortRetryIgnore
        );
    }

    public void TestMenu5()
    {
        MenuBox.Show
        (
            new string[]
            {
                "Option 1\nOption description can go here.",
                "Option 2\nTwo",
                "Option 3\nThree",
                "Option 4\nFour",
                "Option 5\nFive of Nine?",
            },
            new UnityAction[]
            {
                () => MessageBox.Show("You clicked on Option 1"),
                () => MessageBox.Show("You clicked on Option 2"),
                () => MessageBox.Show("You clicked on Option 3"),
                () => MessageBox.Show("You clicked on Option 4"),
                () => MessageBox.Show("You clicked on Option 5"),
            }
        );
    }
```