<template>
  <div id="app">
   <main>

     <div class="search-box">
       <input type="text" class="search-bar" placeholder="Search .."/>
     </div>

     <div class="weather-wrap">
       <div class="location-box">
         <div class="location">Toulouse, FR</div>
         <div class="date">Aujourd'hui</div>
       </div>

       <div class="weather-box">
         <div class="temp">9°c</div>
         <div class="weather">Rain</div>

       </div>
     </div>
   </main>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      api_key: '8d289dcc49d958ac61023631f95ad168'
    }
  }
  
}
</script>

<style>
  *{
    margin:0;
    padding: 0;
    box-sizing: border-box;
  }
  body{
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  }
  #app{
    background-image: url('./assets/cold-bg.jpg');
    background-size: cover;
    background-position: bottom;
    transition: 0.4s;
  }
  main{
    height: 100vh;
    padding: 25px;
    background-image: linear-gradient(to bottom, rgba(0,0,0,0.25),rgba(0,0,0,0.75));
  }
  .search-box{
    width: 100%;
    margin-bottom: 30px;
  }
   .search-bar{
    display: block;
    width: 100%;
    padding: 10px;
    color: #313131;
    font-size: 20px;
    appearance: none;
    border: none;
    outline: none;
    background: none;

    box-shadow: 0px 0px 3px rgba(0,0,0,0.25);
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 0px 16px 0px 16px;
    transition: 0.4s;
  }
  .search-bar:focus{
    box-shadow: 0px 0px 3px rgba(0,0,0,0.25);
    background-color: rgba(255, 255, 255, 0.75);
    border-radius: 16px 0px 16px 0px;
  }
  .location-box .location{
    color: #FFF;
    font-size: 32px;
    font-weight: 500;
    text-align: center;
    text-shadow: 1px 3px rgba(0,0,0,0.25);
  }
 .date{
    color: #FFF;
    font-size: 20px;
    font-weight: 300;
    font-style: italic;
    text-align: center;
    text-shadow: none;
    /* text-shadow: 1px 3px rgba(0,0,0,0.25); */
  }
  .weather-box{
    text-align: center;
    margin-top: 25px;
  }
  .weather-box .temp{
    display: inline-block;
    padding: 10px 25px;
    color: #FFF;
    font-size: 102px;
    font-weight: 900;

    text-shadow: 1px 3px rgba(0,0,0,0.25);  
    background-color: rgba(255, 255, 255, 0.25);  
    border-radius: 30px ;
    box-shadow: 3px 6px rgba(0,0,0,0.25);  

  }
  .weather-box .weather{
    margin-top: 25px;
    color:#FFF;
    font-size: 48px;
    font-weight: 700;
    font-style: italic;
    text-shadow: 1px 3px rgba(0,0,0,0.25);  
  }
</style>
