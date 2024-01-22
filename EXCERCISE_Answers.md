# MERN Excercises

## Excercise : About the API 
Page 100

### 1
using just the URL from the browser results in an error because of the missing Headers, which provide the data of the request (query, mutation). So the simple request with URL only is not working.

### 2
The ability to provide a body to the request. This allows for having a single endpoint but querying different information.

## Excercise : The API List
Page 104
### 1
{IssueList} renders an error message :  
```
"message": "Field \"issueList\" of type \"[Issue!]!\" must have a selection of subfields. Did you mean \"issueList { ... }\"?"
```
Only indicating the issueList field fails because of the missing `arg`

{ issueList { } } does not render anything. No message as we privide an `arg`, but no result as there is no subfield to display.

### 2
{issueList { wrong }} with a wrong subfield, renders an error
```
"message": "Cannot query field \"test\" on type \"Issue\".",
```
which makes sense as the requested subfield is not existing.
The server resonds an error 400. So, yes, the request is sent.
### 3
This is how an aggregated request would look like : 
```
query{
  issueList {
    title
  }
  about
}
```

## Excercise : Custom Scalar Types
### 1
I do not see any difference. 
Probably because ... boooooh :)
### 2
not sure

## Excercise : The Create API

the `due` Date has not been parsed correctly in my case. The result was still a string, exactly as I entered.
This is probably related to the old version running following the book. 
### 1
### 2 
It's passed 1:1 
### 3
### 4

