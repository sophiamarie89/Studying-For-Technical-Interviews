# When to use each data structure

![map cheatsheet](https://qph.ec.quoracdn.net/main-qimg-2435cdfd062fe45ab9da4c2947e65998)

### Hash tables
Hash tables gurantee 3 things:
- 1) Everything in a hash table is part of pair -- there is a **key** and a **value**. You put in and get out data by specifying the key you are operating on.
- 2) If you are doing anything by a single key on a hash table it is stupidly fast. This goes for ``` put(key, value) ``` , ``` get(key) ``` , ``` contains(key) ``` , and ``` remove(key)``` .
- 3) Everything else not listed in #2 is slow.

##### When to use hash tables
- Caching with some frequency, thus optimizing fast look up (i.e. there is a school of students who all have IDs. Caching ``` ID => student ``` makes sense)
- Storing relationships between data, such as when you don't want the objects themselves to be altered/ hold more information
- Performing lots of search operations. Hashtables have O(1) versus ArrayList O(n).

##### When not to use hash tables
- Iterating over the elements (though check out in Java ``` LinkedHashMap ``` )
- Sorting
- Going from value to key. Just make a second hash table.