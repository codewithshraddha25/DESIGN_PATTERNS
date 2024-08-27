# DESIGN_PATTERNS

SOLID principles: mostly used for object oriented design. and coz of it is easy to maintan, scalable and can reuse our code.
SOLID : S-> Single responsibility principle --> principle states that "A class should have only one reason to change"
Ex. Consider A addition class, Addition class should have only one responsibilty that to perform addition, but if addition class is performing subtraction, multiplication etc then it breach SRP.

O - Open and closed Principle --> Principle states that "Software entities like class,module,method should be open for extention but closed for modifications." 
Ex. There is PaymentProcessingSystem which support to process only credit card functionality now its requirement to add debit card functionality in existing system so, there should be different class for debitCardProcessingSystem which can extent existing PaymentProcessing.

L- Liskov's Substitute Principle
Principle says "Derived or child class must be substitutable for their parent class"
Ex. Consider a rectagle can have any hight or width but square is rectangle of having same hight and width so square can extend rectangle ie square is substitute for Rectangle

I-Interface Segregation Principle
Principle is that If any large interface or interface having multiple responsibilities then the interface should split with different interfaces with respective of there own responsibility. make sure interface is having single responsibility.

Ex. Interface Payement is having responsibilities of validation,perform, update,persist and operations like monitoring data, dataAnalyticsUpload so Interface Payemnt should only focus on payment related responsibilities not data related so we need seperate interface to monitor and dataAnalyticsUpload feature

D-Dependency Inversion Principle
Decouple software as much as possible. High level modules should not be dependent on low level modules and both can dependent on abstraction.
ex. In below example class A is loosely couple with class B and dependent on abstraction on Spring container that spring will have created object in container and class A is just using that with the help of autowired
Class A{
 @Autowired
 private B b;

 public void execute(){
 b.show();
 }
}
