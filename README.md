Item Collection
---------------

Item Collections is a dynamic ORMish layer.  It currently sits on top of mysql-native and mdgram, but these could be swapped out for other mechanisms.

The key concepts are Items and Collections.

Items are simply table rows from MySQL, represented in JSON.

Collections are MySQL queries, with an addition.

Queries return one result set, at the time they are executed.  Collections start with the result set, but are then updated by changes coming in over mdgram.

Collections only exists as long as they have subscribers.

Collections are created with two parameters:

a) An SQL query, to generate the intial result set.
b) An ordering function for the collection.
c) A filtering function for the collection.




