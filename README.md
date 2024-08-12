## APIs Easy and Short Method

### GET APIs
```
 static getApi() async {
    final uri = Uri.parse("https://reqres.in/api/users");
    var response = await http.get(uri);

    if (response.statusCode == 200) {
      print('Response data: ${response.body}');
    } else {
      print('Failed to load data. Status code: ${response.statusCode}');
    }
  }
```

### POST APIs
```
static postApi() async {
    final uri = Uri.parse("https://reqres.in/api/register");
    final response = await http.post(
      uri,
      body: {
        "email": "eve.holt@reqres.in",
        "password": "pistol",
      },
    );

    if (response.statusCode == 200) {
      print('Response postApi(): ${response.body}');
    } else {
      print('Failed to load data. Status code: ${response.statusCode}');
    }
  }
```
