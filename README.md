
        REACT : Frond end Technology 
    ------------------------------------

    Basic Commands
    --------------
    1. to create react app : npx create-react-app project-name
    2. to run react app : npm start / npm run dev
    3. install vite: npm i -g create-vite
    4. to create project using vite: npm create vite@latest /
        npm create vite@latest react-app-name -- --template react
    5. to run vite app:  npm run dev
    6. Installing MUI : npm install @mui/material @emotion/react @emotion/styled
    7. Installing React Bootstrap : npm install react-bootstrap bootstrap
        - Add bootstrap themes : using https://bootswatch.com/ website, download bootstrap.min.css file and add it in src folder, import css file into main.jsx
    8. install axios : npm i axios
    9. Install REdux: npm install @reduxjs/toolkit react-redux

    Basic Features
    --------------
    1. Is a collection of JS Libraries : design UI 
    2. Create a single page application : Facebook , Twitter, GMAIL
    3. Features
        - Declarative Approach : 
        - Mutable & Immutable data 
        - Pure Functions : that accept Immutable objects and return a new object that doesnot cause any change
        - JSX (Javascript XML) : ex: const heading = <h1>Heading 1</h1>
            - JSX expressions must be inside a single parent element
            - React fragments : <></> similiar to container tag
            - Changes in attribute : using camel case
                - class become className
                - for become htmlFor
            - to display js expressions isdie JSX : to place js expressions inside {} in JSX Code
            - JSX requires ending tag for all tags : Self closing tags: <tag-name/>
            - to style jsx elements using CSS : 
                - Inline CSS : style should be an object, property should be in camelCase
                - External CSS : import External css file into Components
                - CSS Module : create a file with extension as .module.css
            - Transpiling : conversion of JSX to HTML using babel Library
        - React Components : part of UI, react app is a collection of Components, all the Components are arranged in tree structure, root or parent node : "App" Component
            - to create a Component : create a js/jsx file, filename must starts with capital letter, it always return or render JSX code 
            - Different ways Components
                - Class Based Component / stateful Component
                - Functional Based Component / stateless Component
        - Data sharing Between Components
            - sharing only from Parent to Child : use props
                - props : Property of Component  , its type is object, to access props from Component argument
            - Share data between Sibling : State Lifting
        - React Events handling
            - event binding without argument : event-name={function-name}
            - event binding with argument : event-name={()=>function-name(arg)}
            - event binding with event as argument : event-name={(event)=>function-name(event)}
        - React State : used to store values, it can access and update anywhere in the Component, it will re render Component.
        - React Hooks : To provide react Component Features to function Based Component, is a pre defined function in react, Hooks name always starts with 'use' keyword
            - How to use a Hooks in a Functional based Component
                - it should call the hook at the top level of Component
                - Hooks are not conditional
            - Types of Hooks
                - Predefined Hooks
                    -   useState() : use to create state in Functional based Component
                    -   useEffect(callback,dependency) : used to provide side effects to functional component
                         - Based on depenedency we can provide side effects
                            - if depenedency is not provided, apply side effects all times
                            - if depenedency is empty array : apply side effects at the time of compoenet creation
                            - if depenedency is array with state/props : apply side effects at the time of compoenet creation as well as wnhen values of state/props changes
                    -   useParams() : used to redirect from one location to another
                - Customized hook : function with name starts "use"
        - Conditional rendering : based on a condition we can decide the visiblity of JSX element in DOM
            - if statements :  &&
            - if else statements : ?: ternary
        - Rendering List : use map method, use key attribute to set unique key for each duplicated item
        - Component Life Cycle methods - React Component
            - Mounting Phase : putting all elements into DOM
                - constructor()
                - getDerivedFromProps()
                - render()
                - componentDidMount()
            - Updating Phase : when Component is updated
                - getDerivedStateFromProps()
                - shouldComponentUpdate()
                - render()
                - getSnapshotBeforeUpdate()
                - componentDidUpdate()
            - Unmounting Phase : remove element from DOM
                - componentWillUnMount()
                
        - Functional Based Component            - Class Based Component
        --------------------------------    ---------------------------------
        1. JS Pure function accept props    1. Class extended from react component
         as argument and return jsx          and its render function return jsx
        2. No need of render function to    2. Need render function to return jsx
        to return jsx
        3. Run code from top to bottom,     3. Component alive depending upon its Life
        once jsx returns it cannot alive    Cycle
        4. Stateless Component              4. Stateful Component
        5. hooks used                       5. No need to use hook 
        6. constructor is not available     6. constructor used to assign state

        - React Form 
            - Controlled Component : managed by react compoent, set state to its value field of user inputs
            - Uncontrolled Component : managed by Real DOM
        - Set up path for React component
            - can set up path in App / Root Component
            - Install react-router-dom package : npm i react-router-dom
                - Entire react app should be render in BrowserRouter Selector
                - Place all compenent that need path in Routes Selector
                - Set up path using Route Selector for each component
        - API Call - Axios package
            - install axios
            - Create request instance of axios to make api call


                            --------------------------------------
                                REDUX - STATE MENANGEMENT TOOL 
                            --------------------------------------

        - To avoid props drilling to acheive state management
        - Installation : npm install @reduxjs/toolkit react-redux
        - REDUX TOOLKIT 
            - configureStore() : creating a Redux store
            - Provider from react-redux : Provide store to react App 
            - createSlice() : used to hold both action and reducer together and it return reducer, actions
            - useSelector : hook used to access state from store to compoenet
            - useDispatch : hook used dispatch/execute the action from component

        
