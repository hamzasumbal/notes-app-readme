# Notes API
REST API for managing personal notes.

## Generate API key

```
fetch('https://notes.hamzasumbal.com/api/getapikey')
  .then(response => response.json())
  .then(data => console.log(data));
```

### output

```
{
  message : "The API key is generated, Please save it somewhere safe",
  apiKey  : "YOUR_API_KEY"
}
```

## Create Note

```
fetch('https://notes.hamzasumbal.com/api/create-note', {
  method: 'POST',
  headers: {
      'x-api-key': 'YOUR_API_KEY'
    },
  body : JSON.stringify({
    title : "new title",
    body : "your note here"
  })
}).then(response => response.json())
  .then(data => console.log(data));
```

### output

```
{ 
  message: "Note added successfully" 
}
```


## Delete Note

```
fetch('https://notes.hamzasumbal.com/api/delete-note', {
  method: 'POST',
  headers: {
      'x-api-key': 'YOUR_API_KEY'
    },
  body : JSON.stringify({
    title : "new title",
  })
}).then(response => response.json())
  .then(data => console.log(data));
```

### output

```
{ 
  message: "new title is deleted" 
}
```


## Update Note

```
fetch('https://notes.hamzasumbal.com/api/update-note', {
  method: 'POST',
  headers: {
      'x-api-key': 'YOUR_API_KEY'
    },
  body : JSON.stringify({
    title : "title",
    body : "your note here"
  })
}).then(response => response.json())
  .then(data => console.log(data));
```

### output

```
{ 
  message: "Note updated successfully" 
}
```

## Get Note

```
fetch('https://notes.hamzasumbal.com/api/get-note', {
  method: 'POST',
  headers: {
      'x-api-key': 'YOUR_API_KEY'
    },
  body : JSON.stringify({
    title : "title",
  })
}).then(response => response.json())
  .then(data => console.log(data));
```

### output

```
{ 
  title: "title", 
  body: "your note here" 
}
```

## Get Note List

```
fetch('https://notes.hamzasumbal.com/api/get-note-list', {
  method: 'GET',
  headers: {
      'x-api-key': 'YOUR_API_KEY'
    }
}).then(response => response.json())
  .then(data => console.log(data));
```

### output

```
{ 
  note1: { } , note2: { } , ....
}
```

