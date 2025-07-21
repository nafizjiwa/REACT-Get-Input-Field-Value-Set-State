# REACT-Get-Input-Field-Value-Set-Constant

Usually the first thing a real-world app needs is a way to get user's input. This is commonly done using the HTML <input> element. But a beginner React developer may struggle to get the value of an input field. Here's how to do it:<br>

        import { ChangeEvent, useState } from "react";
        
        function Example() {
          const [inputText, setInputText] = useState("");
        
          const handleChange = (e: ChangeEvent<HTMLInputElement>) => {
            // 👇 Store the input value to local state
            setInputText(e.target.value);
          };
        
          return (
            <div>
              <input type="text" onChange={handleChange} value={inputText} />
        
              {/* 👇 Use the input value from state */}
              <p>Your input: {inputText}</p>
            </div>
          );
        };


### Get the value of an input in React.

#### 1. Create a state variable where you will store the input value.
#### 2. Create a change handler function and set the input value in state with e.target.value
#### 3. Assign the change handler to the onChange prop on the input.
#### 4. Pass the input value as the value prop to the input, or its value won't update.

### Conclusion
This method of event handlers updating the parent component's state and the child elements using getting it as props is an example of React's uni-directional flow.</br>

### 📌Note:
#### The input value will be string even for inputs with type="number" so you may need to convert them to their respective types with Number(e.target.value).
