# 22b01a12b8
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration page</title>
    <link rel="stylesheet" href="styles.css">
    
</head>
<body>
    
    <form action="" onsubmit="return validateform()">

        <div>
            <label for=""style="margin-left: 200px;">Enter Name</label>
            <input type="text" style="margin-left: 100px;" name="" id="name" placeholder="Enter the name">
        </div>
        <br>
        <div>
            <label for="" style="margin-left: 200px;">Enter Passwod</label>
            <input type="password" name=""  style="margin-left: 80px;"id="pass" placeholder="Enter password">
        </div>
        <br>
        <div>
            <label for="" style="margin-left: 200px;">Enter mail</label>
            <input type="email" name="" id="mail" style="margin-left: 110px;" placeholder="Enter the mail">
        </div>
        <br>
        <div>
            <label for="" style="margin-left: 200px;">Phone Number</label>
            <input type="number" name="" id="no" style="margin-left: 83px;" placeholder="Enter the mobilenumber">
        </div>
        <button type="submit"style="margin-left: 200px;" onclick="return validateform">Submit</button>
        <span id="errorm"></span>
       
    </form>
    <script>

        function validateform()
        {
            let name1 = document.getElementById("name");
            let mail1 = document.getElementById("mail");
            let mobile_no1=document.getElementById("no");
          let password1= document.getElementById("pass");
          let error1 =document.getElementById("errorm");
         let nameregex=/^[a-zA-Z ]+$/;
          if((name1.value===""))
          {
             
              
              error1.textContent="name field must be filled"
              return false;

          }
          
          if(name1.value.length<8)
         {
            error1.textContent="name should greater than 8"
            return false
         }
         if(password1.value==="")
         {
            error1.textContent="password cannot be empty and grater than 8 characters";
            return false;
         }
         if(password1.value.length<8)
         {
            error1.textContent="password should greater than 8"
            return false;
         }
         if(mobile_no1.value.length>10|| mobile_no1.value.length<10)
         {
            error1.textContent="mobile number must 10 characters";
            return false;
         }
         if(mail1.value==="")
         {
            error1.textContent="Enter the mail";
            return false;
         }
         if(!(nameregex.test(name1.value)))
         {
            error1.textContent="Enter the alpabets in name field";
            return false;
         }

alert("form submitted");
return true;
        

        }

      </script>
</body>
</html>
