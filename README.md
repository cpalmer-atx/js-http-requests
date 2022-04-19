# JavaScript HTTP Requests

<p align="center">Compliments of RapidAPI, this repo serves as a quick reference for different HTTP request options using JavaScript.</p>

<br><div align="center">Visit
<a href="https://rapidapi.com">RapidAPI</a>
</div><br>

## 1. XMLHttpRequest

```
var xhttp = new XMLHttpRequest();
xhttp.onreadystatechange = function() {
    if (this.status === 200) {
        console.log(xhttp.responseText);
    }
};

xhttp.open("GET", "URL");
xhttp.send();
```

## 2. Fetch API

```
fetch(URL)
    .then( res => {
        console.log(res)
    })
    .catch( err => {
        console.log(err)
    });
```

## 3. Axios

```
import axios from 'axios';

const requestData = async () => {
    try {
        const res = await axios.get('API', {
            headers: {},
            params: {}
        });
    } catch(err) {
        console.log(err);
    }
}
```

## 4. jQuery AJAX

```
$.ajax({
    url: 'URL',
    type: 'GET',
    success: function (response) {
        console.log(response);
    },
    error: function (error) {
        console.log(error);
    },
});
```
