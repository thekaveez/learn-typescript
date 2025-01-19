
# Typescript




## Variables

```bash
let myName: string = "Bob"
let numberOfWheels: number = 4
let isStudent: boolean = false

```
## Custom Types

```bash
type Person = {
    name: string
    age: number
    isStudent: boolean
}

let person1: Person = {
    name: "Joe",
    age: 42,
    isStudent: true
}

let person2: Person = {
    name: "Jill",
    age: 66,
    isStudent: false
}

```
## Nested Object Types

```bash
type Address = {
    street: string
    city: string
    country: string
}

type Person = {
    name: string
    age: number
    isStudent: boolean
    address: Address
}

let person1: Person = {
    name: "Joe",
    age: 42,
    isStudent: true,
    address: {
        street: "123 Main",
        city: "Anytown",
        country: "USA"
    }
}

let person2: Person = {
    name: "Jill",
    age: 66,
    isStudent: false,
    address: {
        street: "123 Main",
        city: "Anytown",
        country: "USA"
    }
}

```
## Typing Arrays

```bash
type Person = {
    name: string
    age: number
    isStudent: boolean
}

let person1: Person = {
    name: "Joe",
    age: 42,
    isStudent: true,
}

let person2: Person = {
    name: "Jill",
    age: 66,
    isStudent: false,
}

let people: Person[] = [person1, person2]

let people: Array<Person> = [person1, person2]

```
## Literal Types

```bash
let userRole: "member" = "member"

```

## Unions

```bash
type UserRole = "guest" | "member" | "admin"

let userRole: UserRole = "member"

```
## Type Narrowing

```bash
function getPizzaDetail(identifier: string | number) {
    if (typeof identifier === "string") {
        return menu.find(pizza => pizza.name.toLowerCase() === identifier.toLowerCase())
    } else {
        return menu.find(pizza => pizza.id === identifier)
        
    }
}

```
## Function Return Types

```bash
function fetchUserDetails(username: string): User {
    const user = users.find(user => user.username === username)
    if (!user) {
        throw new Error(`User with username ${username} not found`)
    }
    return user

```

