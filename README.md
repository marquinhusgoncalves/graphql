run `npm run dev``
run `npm run json:server`

and open `http://localhost:4000/graphql`


## schema  User

```
{
  user(id: "23") {
    id
    firstName
    age
  }
}
```
## schema  Company

```
{
  company(id: "1") {
    id
    description
    name
  }
}
```

## schema Company with fragment

```
{
  apple: company(id: "1") {
    ...companyDetail
  }
  google: company(id: "2") {
    ...companyDetail
  }
}

fragment companyDetail on Company {
  id
  description
  name
  users {
    id
    firstName
    age
  }
}
```
