# Event-organization
Introduction:-
This project is a basic implementation of an event management system using Solidity. The contract allows event organizers to create events, set ticket prices and quantities, and manage ticket sales. Users can buy and transfer tickets to events.

Contract:-
The contract is located in the contracts folder and is named EventContract.sol. It has the following functions:
createEvent: allows event organizers to create new events
buyTicket: allows users to buy tickets to events
transferTicket: allows users to transfer tickets to other users

How it Works:-
Event organizers create new events using the createEvent function, specifying the event name, date, price, and ticket quantity.
Users can buy tickets to events using the buyTicket function, specifying the event ID and quantity of tickets to purchase.
The contract checks that the event exists, has not already occurred, and that the user has sent enough ether to cover the ticket price.
If the purchase is successful, the contract updates the event's ticket remaining count and adds the tickets to the user's ticket balance.
Users can transfer tickets to other users using the transferTicket function, specifying the event ID, quantity of tickets to transfer, and the recipient's address.
The contract checks that the user has enough tickets to transfer and updates the ticket balances accordingly.

Structures:-
The contract uses two structures:
Event: represents an event, with fields for the organizer's address, event name, date, price, ticket count, and remaining tickets.
tickets: a mapping of user addresses to event IDs, with fields for the quantity of tickets held by each user for each event.

Variables:-
The contract has two public variables:
events: a mapping of event IDs to Event structures.
nextId: a counter for the next event ID.
tickets: a mapping of user addresses to event IDs, with fields for the quantity of tickets held by each user for each event.

Security:-
This contract has not been audited and should not be used in production without further testing and review.

Code
The contract code is located in the contracts folder and is named Event.sol.
