
<!DOCTYPE html>
<html>     
 <head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
<body >

<form method="post" action="index.php"><br/><br/>
<table>
<tr>

<td> To:</td>
<td> <textarea name="mail_to" cols="40" rows="5"></textarea> </td>
</tr>
<tr>

<td>  Subject</td>
<td> <textarea name="mail_sub" cols="40" rows="5"></textarea> </td>
</tr>
<tr>

<td > Message:</td>
<td>  <textarea name="mail_msg" cols="40" rows="5"></textarea> </td>
</tr>
<tr>

<td colspan="2" > <input type="submit" name="Submit" value="Send Email"></td>
 
</tr>

</table>
  
   
  
 </form>
 
     
</body>
</html>
 <?php
if(!(isset($_POST['mail_to'])) || !(isset($_POST['mail_sub'])) || !(isset($_POST['mail_msg']))  ){
 echo "Neede parameters has not been set";
}
   
else {
	 
	 $mt=$_POST['mail_to'];
	$ms=$_POST['mail_sub'];
	$mm=$_POST['mail_msg'];
 if(($mt=="") || ($ms=="") || ($mm=="")  ){
 echo "Please fill all fields";
 }
else {
	
	

	$mail= mail('mahammad.yagubli@gmail.com',$ms,$mm,'From: mahammad.yagubli@gmail.com');
	if($mail){echo "Mail is Sent";}
	
	else {echo "Mail is Sent";}
	   
   }
	
	
	
}
?>
