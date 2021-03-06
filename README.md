# Introduction

_This package is meant to provide an easy way to create and use a database, **all data is stored persistently**, and comes with additional easy to use features._

**Installation**

```ruby
npm install quick.db
```

**Require Package**

```javascript
var db = require('quick.db')
```

## What is Quick.db?

> Quick.db is an easy-to-use database manager built with better-sqlite3. It's simple by design and perfect for smaller projects where you don't want to set up a separate database server or individuals who may be getting started with programming.

## Example

> _All data in quick.db is stored **persistently** in a database. Here is an example of setting an object in the database, then fetching parts & the full object._

```javascript
const db = require('quick.db');

// Setting an object in the database:
db.set('userInfo', { difficulty: 'Easy' })
// -> { difficulty: 'Easy' }

// Pushing an element to an array (that doesn't exist yet) in an object:
db.push('userInfo.items', 'Sword')
// -> { difficulty: 'Easy', items: ['Sword'] }

// Adding to a number (that doesn't exist yet) in an object:
db.add('userInfo.balance', 500)
// -> { difficulty: 'Easy', items: ['Sword'], balance: 500 }

// Repeating previous examples:
db.push('userInfo.items', 'Watch')
// -> { difficulty: 'Easy', items: ['Sword', 'Watch'], balance: 500 }
db.add('userInfo.balance', 500)
// -> { difficulty: 'Easy', items: ['Sword', 'Watch'], balance: 1000 }

// Fetching individual properties
db.get('userInfo.balance') // -> 1000
db.get('userInfo.items') // -> ['Sword', 'Watch']

// Showing dot notation setting
db.set('userInfo.difficulty', 'Hard')
// -> { difficulty: 'Hard', items: ['Sword', 'Watch'], balance: 1000 }

db.get('userInfo.difficulty') // -> 'Hard'
```

## Our Sponsor

**Need A VPS?** Get started with **Contabo**!   Up to 60 GB RAM - 10 Cores - Unlimited Traffic   **Starting at €3.99**  

[**Click To Learn More & View Prices**](http://www.anrdoezrs.net/click-9103034-12740668)

