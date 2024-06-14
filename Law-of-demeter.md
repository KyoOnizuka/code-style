##Understanding the Law of Demeter
For all classes C, and for all methods M attached to C, all objects to which M sends a message must be instances of classes associated with the following classes:

The argument classes of M (including C)
The instance variable of classes of C
(Objects created by M, or by functions or methods which M calls, and objects in global variables are considered as arguments of M.)

#Simply put, the Law says that a method X of class C should only invoke the methods of:

Class C itself
An object created by X
 An object passed as an argument to X
 An object held in an instance variable of C
A static field
