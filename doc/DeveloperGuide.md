# Developer Guide

* [Setting Up](#setting-up)
* [Design](#design)
* [Testing](#testing)
* [Appendix A: User Stories](#appendix-a--user-stories)
* [Appendix B: Use Cases](#appendix-b--use-cases)
* [Appendix C: Non Functional Requirements](#appendix-c--non-functional-requirements)
* [Appendix D: Gloassary](#appendix-d--glossary)

## Setting up

#### Prerequisites

1. **JDK 8** or later 
2. **Eclipse** IDE
3. **e(fx)clipse** plugin for Eclipse (Do the steps 2 onwards given in 
   [this page](http://www.eclipse.org/efxclipse/install.html#for-the-ambitious))


#### Importing the project into Eclipse

0. Fork this repo, and clone the fork to your computer
1. Open Eclipse (Note: Ensure you have installed the **e(fx)clipse plugin** as given in the prerequisites above)
2. Click `File` > `Import`
3. Click `General` > `Existing Projects into Workspace` > `Next`
4. Click `Browse`, then locate the project's directory
5. Click `Finish`

## Design
<img src="images/mainClassDiagram.png"/>

## Testing

* In Eclipse, right-click on the `test/java` folder and choose `Run as` > `JUnit Test`

## Appendix A : User Stories

Priorities: High (must have) - `* * *`, Medium (nice to have)  - `* *`,  Low (unlikely to have) - `*`


Priority | As a ... | I want to ... | So that I can...
-------- | :-------- | :--------- | :-----------
`* * *` | user | store name, email, phone number, address, tag words for each new contact added | 
`* * *` | new user | see usage instructions | refer to instructions when I forget how to use the App
`* * *` | user | add a new person | 
`* * *` | user | delete a person | can remove entries that I no longer need
`* * *` | user | find a person by name | locate details of persons without having to go through the entire list
`* * *` | user | edit the information of an existing contact | update contact information of people
`* * *` | user | categorize contacts | classify contacts as friends, colleagues, acquaintances, etc.
`* * *` | user | view contacts by category in a tabular format | view list of friends at a time for instance, etc.
`* * *` | user | view all contacts at once in a tabular format | view a list of all contacts in the address book
`* *` | user | add notes/tags to each contact optionally | mark some contacts with tag words they are associated with
`* *` | user | have multiple address books and ask the user to open a certain address book at the start of the system | 
`* *` | user | hide [private contact details](#private-contact-detail) by default | to minimize chance of someone else seeing them by accident
`*` | user with many persons in the address book | sort persons by name | locate a person easily
`*` | user | export a list of specific information of contacts (categorized) to a file in a specified directory | collect only certain information such as only name or phone number of contacts and store the information in a file in the directory of my choice
`*` | user | import a list of contacts from an external file into the address book | add contacts stored somewhere else quickly to this address book
`*` | user | skype call any of the contacts | quickly call anyone in the address book on skype using skype credit

## Appendix B : Use Cases

(For all use cases below, the **System** is the `AddressBook` and the **Actor** is the `user`, unless specified otherwise)

#### Use case: Delete person

**MSS**

1. User requests to list persons
2. AddressBook shows a list of persons
3. User requests to delete a specific person in the list
4. AddressBook deletes the person <br>
Use case ends.

**Extensions**

2a. The list is empty

> Use case ends

3a. The given index is invalid

> 3a1. AddressBook shows an error message <br>
  Use case resumes at step 2

## Appendix C : Non Functional Requirements

1. Should work on any [mainstream OS](#mainstream-os) as long as it has Java 8 or higher installed.
2. Should be able to hold up to 1000 persons.
3. Should come with automated unit tests and open source code.
4. Should favor DOS style commands over Unix-style commands.

## Appendix D : Glossary

##### Mainstream OS

> Windows, Linux, Unix, OS-X

##### Private contact detail

> A contact detail that is not meant to be shared with others

