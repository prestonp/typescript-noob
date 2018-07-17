i don't know how to typescript so i'm collecting all of the weird syntax errors i don't understand as a reference guide.

# object implicitly has an 'any' type

```
const phonebook = {
    jim: 2813308004,
    pam: 7133211234,
}

const getNumber = (person : string) => phonebook[person] // Index signature of object type implicitly has an 'any' type:
```

Add an index signature to the object

```
interface Phonebook {
    [key: string]: number;
}

const phonebook: Phonebook = {
    jim: 2813308004,
    pam: 7133211234,
}

const getNumber = (person : string) => phonebook[person]
```
