# Code Examples
  - [Array List](#ast) 
  - [Hashtable](#ht)

## Array List {#ast}
```
#include "Set.h"

/**
 * Implement the ArrayListSet methods correctly
 */
unsigned int ArrayListSet::size() {
    return arr.size();
}

void ArrayListSet::insert(string s) {
    for(vector<string>::iterator it = arr.begin(); it != arr.end(); it++){
        if(*it == s){
            return;
        }
    }
    arr.push_back(s);
}

void ArrayListSet::remove(const string & s) {
     for(vector<string>::iterator it = arr.begin(); it != arr.end();){
        if(*it == s){
            it = arr.erase(it);
            return;
        }
        else{
            it++;
        }
    }
}

bool ArrayListSet::find(const string & s) {
    for(vector<string>::iterator it = arr.begin(); it != arr.end(); it++){
        if(*it == s){
            return true;
        }
    }
    return false;
}

```


## Hashtable {#ht}
```
#include "Set.h"

/**
 * Implement the HashTableSet methods correctly
 */
unsigned int HashTableSet::size() {
    return ht.size();
}

void HashTableSet::insert(string s) {
    ht.insert(s);
}

void HashTableSet::remove(const string & s) {
    ht.erase(s);
}

bool HashTableSet::find(const string & s) {
    for(auto it = ht.begin(); it != ht.end(); it++){
        if(*it == s){
            return true;
        }
    }
    return false;
}
```

