# Assignment12-Let's Build Our Store
## Theory

Qn1.useContext vs Redux?

- useContext is a hook that provides a way to pass data through the component tree without manually passing props down through each nested component.It is used for smaller applications to share data.

- Redux is a state management library.It is used to manage and share data.It is used for bigger applications but it is complex to understand.

Qn2.Advantages of using redux toolkit over redux?

- Configuring a Redux store is too complicated
- Have to add a lot of packages to build a large scale application
- Redux requires too much boilerplate code which makes it cumbersome to write efficient and clean code.


Qn3. Explain Dispatcher?

- The dispatch function accepts an object that represents the type of action we want to execute when it is called. 
- Basically, it sends the type of action to the reducer function to perform its job, which, of course, is updating the state
- const dispatch=useDispatch();
- dispatch(action(payload))

Qn4.Explain Reducer?

- Reducers are functions that take the current state and an action as arguments, and return a new state result.
- (state,action)=>{}

Qn5. Explain Slice?

- A "slice" is a collection of Redux reducer logic and actions for a single feature in your app, typically defined together in a single file.


Qn6. Explain Selector?

- A “selector” is simply a function that accepts Redux state as an argument and returns data that is derived from that state.
- useSelector(store=>store.cart.items)

Qn7. Explain createSlice and the configuration it takes?

- createSlice is a higher order function that accepts an initial state, an object full of reducer functions and a slice name.

- createSlice({
- name:"cart",
- initialState:{
-    items:[]
- },
- reducers:{
-    addItem:(state,action)=>{},
-    clearItem:(state)=>{}
- }
- })
- export const {addItem,clearItem}=cartSlice.actions;
- export default cartSlice.reducer;
