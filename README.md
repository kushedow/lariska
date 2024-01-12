# lariska
Lariska.js is a micro-framework designed for rapid development of socket-based applications.  It features routing, templating, and state management, along with configurable payload options for outgoing requests, streamlining the development of real-time, interactive applications.

### Starting Up

Javascript
```
app = new Lariska({
  store: {appName: "Hello Lariska"},
  container: "#app",
  pages: {main: {}},
  url: 'http://0.0.0.0'
});

app.go("main")

```

HTML container
```
<main id="app">
</main>
```
HTML Templates
```
<template id="main">
  {{appName}}
</template>
```

### Route

```
app.go(page to go to)
```

### Emit socket events

```
app.emit(event, data)
```

### Add store keys to send with every emit

```
app.addPayload(key)
```

### Handle socket events

```
app.on(event, page to open after handling (optional), callback (optional))
```

### Create handlers

```
app.addHandler("name", callback)
```

### Trigger handlers
```
app.run("name", data)
```

### Handle dom events

```
onclick="app.go('standby')" 
onclick="app.emit('update')" 
onclick="app.run('pickQuestion')"
```

