# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
✓ Create a TicketMachine object on the object bench.
✓ Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
✓ Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
✓ Use `insertMoney` method to simulate inserting an amount of money into the machine.
✓ Use `getBalance` to check that the machine has a record of the amount inserted.
	✓ You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
	:0

### Exercise 2.3
✓ Experiment with inserting different amounts of money before printing tickets.
	✓ Do you notice anything strange about the machine’s behavior?
		:The machine doesn't need any specific balance to print a ticket. It will print with 0 cents balance even.
	✓ What happens if you insert too much money into the machine – do you receive any refund?
		:No refunds are given.
	✓ What happens if you do not insert enough and then try to print a ticket?
		:A ticket will print anyway.

### Exercise 2.4
✓ Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
✓ Create another ticket machine for tickets of a different price.
	✓ Buy a ticket from that machine.
	✓ Does the printed ticket look different?
		:Yes, the price on the ticket has changed.

### Exercise 2.6
✓ Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
		

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?
	:Yes, lots of things get underlined in red.

✓ Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	✓ Do you notice a change in the class diagram?
		:Yes, TicketMachine class is crossed out with red x's.
	✓ What error message do you get when you now press the compile button?
		:Several, but the first is `<identifier> expected`
	✓ Do you think this message clearly explains what is wrong?
		:Somewhat, it's expecting an identifier as the next word but instead I gave it a reserved word which can't be an identifier.

### Exercise 2.8
✓ Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
	:yes.

### Exercise 2.9
✓ From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
		:Fields: price, balance, total
		:Constructor(s): TicketMachine(int x)
		:methods: int getPrice(), int getBalance(), void insertMoney(int n), void printTicket(),

### Exercise 2.10
✓ Do you notice any features of the constructor that make it significantly different from the other methods of the class?
	:Has the same exact name, lacks a return type.

### Exercise 2.11
✓ What do you think is the type of each of the following fields?

```java
private int count; 				//int (integer)
private Student representative; //Student
private Server host; 			//Server
```

### Exercise 2.12
✓ What are the names of the following fields?

```java
private boolean alive;	//alive
private Person tutor;	//tutor
private Game game;		//game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
	:yes
✓ Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	✓ Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
	:yes, red x's will not be able to compile, gray hashes are able to compile
	✓ Check by pressing the compile button to see if there is an error message.
	✓ Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
✓ Is it always necessary to have a semicolon at the end of a field declaration?
	:yes
✓ Once again, experiment via the editor.
✓ The rule you will learn here is an important one, so be sure to remember it.
	:finish statements with a ';'


### Exercise 2.15
✓ Write in full the declaration for a field of type `int` whose name is `status`.
	```java
	public class SomeClass {
		private int status;
	}
	```

### Exercise 2.16
✓ To what class does the following constructor belong?
```
public Student(String name) //class Student (they share the name)
```

### Exercise 2.17
✓ How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)    //2 parameters, title is a String, price is a double
```

### Exercise 2.18
✓ Can you guess what types some of the `Book` class’s fields might be?
	:Many of them would be String, some would be ints, you might have fields of nested class types that are composed of Strings and ints as well.
✓ Can you assume anything about the names of its fields?
	:You would probably have fields like author(s), title, publication year, copyright year, ISBN, content

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.

### Exercise 2.19
```
public class Pet {
	String name;
	public Pet(String startingName){
		name = startingName;
	}
}
```

### Exercise 2.21
✓getPrice() and getBalance() are largely the same except they return difference values (price vs. balance)

### Exercise 2.22
✓getBalance() can be characterized as "How many cents are there stored in the balance toward the current ticket"

### Exercise 2.23
✓If the name of getBalance is changed to get amount, the return statement in the body doesn't need to be changed.

### Exercise 2.24
```
public int getTotal(){
        return total;
    }
```

### Exercise 2.25
✓Error: Missing return statement

### Exercise 2.26
✓getPrice() returns an int and doesn't modify the object. printTicket returns void and does modify the object (mutator method)

### Exercise 2.27
✓insertMoney() and printTicket() both do not have return statements. They return type `void` in the header, so it tells you they don't have a return statement.

### Exercise 2.28
✓did it

### Exercise 2.29
```
public void setPrice(int ticketCost){/*...*/}
//you know it's a method not a constructor because it specifies a return type and conventionally constructors use capital first letter. (not a must)
```

### Exercises 2.30
```
public void setPrice(int ticketCost){
        price = ticketCost;
    }
```

### Exercises 2.31
```
public void increase(int points){
	score += points;
}
```

### Exercises 2.32
```
public void discount(int amount){
        price -= amount;
        if (price < 0) {
            price = 0;
        }
    }
```

### Exercised 2.33
```
public void prompt(){
        System.out.println("Please insert the correct " +
            "amount of money");
    }
```

### Exercises 2.34
```
public void showPrice(){
        System.out.println("The price of a ticket is " + 
            price + " cent(s).");
    }
```

### Exercises 2.35
Differently priced ticket machines return different numbers for showPrice(). This is because the methods called are specific to the object they were called on.

### Exercised 2.36
`you'd get "# price cents" instead. It wouldn't evaluate price anymore`

### Exercise 2.37
`same thing`

### Exercise 2.38
`They wont show anything useful. "price" is just a string literal in both cases and won't evaluate to anything useful.`

### Exercise 2.39
```
public TicketMachine()
    {
        price = 1000;
        balance = 0;
        total = 0;
        
    }
```
`now when you construct a ticketmachine it's ticket price is set automatically to 1000`

### Exercise 2.40
```
public void empty(){
        total = 0;
    }
```
`this is a mutator`

### Exercise 2.41
```
public void setPrice(int ticketCost){
        price = ticketCost;
    }
```
`This is a mutator`

### Exercise 2.42
```
public TicketMachine()
    {
        price = 1000;
        balance = 0;
        total = 0;
        
    }
    
    public TicketMachine(int startingPrice){
        price = startingPrice;
        balance = 0;
        total = 0;
    }
```
`they work as expected`

### Exercise 2.43
`balance will not change if an error is printed, adding zero cents doesn't change the balance and prints an error`

### Exercise 2.44
`adding zero cents will not give an error anymore. Balance will be updated but won't change`

### Exercise 2.45
`isVisible, a bool is a good choice because it will only be one of two values at a time`

### Exercise 2.46
✓

### Exercise 2.47
`no, balance must be at least equal to price before a ticket can be printed in the first place`

### Exercise 2.48
` "+,-,*,/,%"`

### Exercise 2.49
`int saving = price * discount`

### Exercise 2.50
`int mean = total / count;`

### Exercise 2.51
`if (price > budget) {Sout("too expensive")} else {Sout("Just right")}`

### Exercise 2.52
`if (price > budget) {Sout("too expensive, budget = " + budget)} else {Sout("Just right")}`

### Exercise 2.53
`because the new method doesn't use a placeholder variable for the balance to refund before resetting it to zero`

### Exercise 2.54
`It won't compile, the return statement is the final statement in a method, there shouldn't be anything after it.`

### Exercise 2.55
```
public int emptyMachine(){
    int temp = total;
    total = 0;
    return temp;
}
```

### Exercise 2.56
`Both, it returns the value of a private member variable (getter/accessor) and it modifies private fields of the object (setter/mutator)`

### Exercise 2.57
```
public void printTicket(){
    int amountLeftToPay = price - balance;
    if(amountLeftToPay <= 0) {
        // Simulate the printing of a ticket.
            System.out.println("##################");
            System.out.println("# The BlueJ Line");
            System.out.println("# Ticket");
            System.out.println("# " + price + " cents.");
            System.out.println("##################");
            System.out.println();
            // Update the total collected with the price.
            total = total + price;
            // Reduce the balance by the price.
            balance = balance - price;
    } else {
        System.out.println("You must insert at least: " +
(price - balance) + " MORE cent(s).");
    }
}
```


READ upto and INCLUDING section 2.15 of this chapter.