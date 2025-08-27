<App>
 └─ <NavigationContainer>
      └─ <Stack.Navigator>
           ├─ <HomeScreen>
           │    └─ <ProductCard>
           └─ <DetailScreen>
I am using <App> as the root component of my application. Inside it, I wrap everything in a NavigationContainer so that I can manage screen navigation using React Navigation.

I created a stack navigator (<Stack.Navigator>) to handle transitions between screens. My two main screens are HomeScreen and DetailScreen.

In the HomeScreen, I fetch all the products from the FakeStore API and store them using useState. I then display the products in a grid. For each product, I pass its data as props to a <ProductCard> component, which shows the product’s image and name. I also set it up so that when a user taps a product, it navigates to the DetailScreen.

In the DetailScreen, I receive the product ID via route parameters, and I fetch the full details of that product from the API. I use useState again to hold the product details, and then I display the product image, title, price, and description in a clean mobile layout.

This structure allows me to manage state effectively, pass data via props, and enable smooth navigation between the product list and product details.