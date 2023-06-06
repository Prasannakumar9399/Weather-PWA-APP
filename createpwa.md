(1)Adding the service worker.

Service worker is a javascript file that runs all the time as soon as we open the page or we close the page for that exact reason service worker helps us with lot of reasons. Example:push notification,offline support.

Add this in index.html

 <script>
      if('serviceWorker' in navigator){
        window.addEventListener('load',()=>{
          navigator.serviceWorker.register('./serviceworker.js').then((reg)=>console.log(reg.scope)).catch(err=>console.log(err));
        })
      }
    </script>
Then we will write code in serviceworker.js check the code in serviceworke.js

(2)Create manifest.json 
