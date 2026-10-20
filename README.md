
# Practical 9 - React Hooks Example

## a1.html

```html
<!DOCTYPE html>
<html>
<head>
    <title>React Hooks Example</title>

    <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>

    <!-- This loads the React library version 18 from the internet. -->

    <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>

    <!-- ReactDOM connects the React component to the HTML page (DOM) -->

    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>
<body>

    <div id="root"></div>

    <script type="text/babel">
        function App() {
            const [color, setColor] = React.useState("");

            return (
                <div style={{ textAlign: "center", marginTop: "50px" }}>
                    <h2>Select a Color</h2>

                    <button onClick={() => setColor("Red")}>Red</button>
                    <button onClick={() => setColor("Blue")}>Blue</button>
                    <button onClick={() => setColor("Green")}>Green</button>
                    <button onClick={() => setColor("Yellow")}>Yellow</button>

                    {color && <h3>You have selected {color}</h3>}
                </div>
            );
        }

        const root = ReactDOM.createRoot(document.getElementById("root"));
        root.render(<App />);
    </script>

</body>
</html>
```
