**Code Example**

```

This is the top level required function in dart.


void main() {
  
print("caleb is a great flutter developer");
  
}

It is the programme starting point.

Void means that the function does not return anything.

```

**Variables**

```
Dart is a statically typed language.

This means that the datatype of a variable is known and determined at compile time rather than at runtime.

Once we declare a variable and give it a type eg string we cannot change the value to another datatype in the future.

int , String and boolean

void main() {

  bool isNight =true;
  
  print(isNight);
  
  
}

Another type of a variable is called dynamic
Means we can change the datatype in the future.

You should avoid using dynamic variables.
This negates the benefits of a dynamically typed programming language.

void main() {

  dynamic name =89;
  
  name='mbugua';
  print(name);
  
  
}

```

***Functions***

(a)Example One

```
void main() {

  String greet = greeting();
  
 int age = getAge();
  
  print(age);
  print(greet);
}


String greeting(){
  
  return "hello";
}

int getAge(){
  
  return 24;
}

```

(b)Example Two

```
When you do not have a lot of values to return you may return thr values from inside an arrow
function.

void main() {

  String greet = greeting();
  
 int age = getAge();
  
  print(age);
  print(greet);
}



String greeting() => 'hello';

int getAge() =>24;

```

**Lists**
```
It is very good practice to declare the datatype of the list.

List<String> names = ['caleb','mercy','karanja'];

This restricts to only string datatypes in the list.

```

**Example**
```
void main() {

  List<String> names = ['caleb','mercy','karanja'];
  
  //List methods
  //adding to the List.
  names.add('luigi');
  names.remove("caleb");
  
  print(names);
  
}

```

**Classes**
```
Classes are basically a blue print to an object.

```

**Simple class**
```

void main() {

  //Instantiating a class
  User userone=User();
  
  //calling an attribute/property of the class
  print(userone.username);
  print(userone.age);
  
  //Invoking a function from the class
  userone.login();
}


class User {
  
  String username ='Caleb';
  int age =24;
  
  void login (){
    
    print('user logged in');
  }
  
}


The disadvantage with this is that each time i instantiate a class it will always have the same value.

This is solved by introducing a constructor to a class.

You can dynamically make many instances of the class(objects) using a constructor.

```

**Simple class with a constructor**
```

void main() {

  //Instantiating a class
  User userOne=User('caleb', 24);
  
  //calling an attribute/property of the class
  print(userOne.username);
  print(userOne.age);
  
  User userTwo = User('mercy',23);
  
  print(userTwo.username);
  print(userTwo.age);
  
  //Invoking a function from the class
  userOne.login();
}


class User {
  
  //class attributes
  String username;
  int age ;
  
  //constructor function
  //Should have the same name as the class
  //It is a special type of function therefore 
  //does not take void
  User(String username , int age ){
    this.username =username;
    this.age=age;
    
  }
  void login (){
    
    print('user logged in');
  }
  
}

```


**Inheritance Example**
```

void main() {

  //Instantiating a class
  User userOne=User('caleb', 24);
  
  //calling an attribute/property of the class
  print(userOne.username);
  print(userOne.age);
  
  User userTwo = User('mercy',23);
  
  print(userTwo.username);
  print(userTwo.age);
  
  //Invoking a function from the class
  userOne.login();
  
  
  
  /*Inheritance*/
  
  SuperUser userThree = SuperUser("Humphrey",58);
  
  print(userThree.username);
 
  /*Invoking the extra method from the inherited class*/
  
  userThree.publish();
  
  /*has access to methods from the parent class*/
  
  userThree.login();
  
}


class User {
  
  //class attributes
  String username;
  int age ;
  
  //constructor function
  //Should have the same name as the class
  //It is a special type of function therefore 
  //does not take void
  User(String username , int age ){
    this.username =username;
    this.age=age;
    
  }
  void login (){
    
    print('user logged in');
  }
  
}

/*Inheritance*/

/*The SuperUser class wants to inherit from the User
 but have some added functionlities which a normal
 user should not have
 */
class SuperUser extends User{
 
  //super calls the constructor from the class it extends from
  //and passes those values in.
  /* We as well inherit the functions of the previous
  class plus it now has an added function/method.
  */
  
  SuperUser(String username, int age ):super(username,age);
  
  void publish (){
    print("published update!");
  }
}

```