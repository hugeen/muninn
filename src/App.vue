<template>
  <div id="app">
    <header>
      <ul id="navbar">
        <li><router-link to="/" exact>Home</router-link></li>
        <li><router-link to="/koin" exact>Notes</router-link></li>
        <li><a href="#">Todos</a></li>
        <li><a href="#">About</a></li>
      </ul>
    </header>
    <div id="wrapper">
      <router-view></router-view>
    </div>
  </div>
</template>


<script>
export default {
  name: 'app'
}
</script>

<style>
body {
    background-color: #fbeed7;
    font-family: 'Raleway', sans-serif;
    font-size: 17px;
}

#navbar {
    background-color: #ffba5a;
    position: absolute;
    height: 50px;
    width: 100%;
    color: white;
    list-style-type: none;
    margin: 0;
    padding: 0;
    top: 0;
    left: 0;
}

#navbar li {
    float: left;
}

#navbar li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
    -webkit-transition-duration: 0.4s; /* Safari */
    transition-duration: 0.4s;
}

#navbar li a:hover {
    background-color: #ff7657;
}

#navbar .router-link-active {
    background-color: #665c84;
}


#wrapper {
    position: absolute;
    top: 50px;
    left: 0;
    width: 100%;
}


#new-note {
    height: 200px;
    width: 60%;
    border-radius: 10px;
    border: 5px solid #ff7657;
    outline-style: none;
}

.indiv-note {
    background-color: white;
    border-radius: 10px;
    height: 100px;
    width: 60%;
    padding-left: 15px;
    margin: 10px;
    border-left: 5px solid #ff7657;
    border-right: 5px solid #ff7657;
    list-style-type: none;
    overflow: auto;
}

.indiv-note .update {
    font-style: italic;
    font-size: 0.6em;
    float: right;
    padding-right: 5px;
}

.indiv-note .note-content {
    height: 80px;
    overflow: hidden;
}

.indiv-note .far {
    float: right;
    padding-right: 5px;
    font-size: 2em;
    color: #ffba5a;
}

.indiv-note .fas {
    float: right;
    padding-right: 5px;
    font-size: 2em;
    color: #ffba5a;
}


button {
    display: block;
    height: 50px;
    width: 150px;
    background-color: #ff7657;
    color: white;
    text-transform: uppercase;
    border-radius: 10px;
    border: none;
}

button i {
    float: right;
}

#note-edit textarea {
    height: 200px;
    width: 60%;
    border-radius: 10px;
    border: 3px solid #ff7657;
    outline-style: none;
}

#note-display {
    border-radius: 10px;
    border: 5px solid #ff7657;
    background-color: white;
    height: auto;
    padding: 10px;
}
</style>
