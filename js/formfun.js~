var temp=0;
var temp1=11.111111111;
var fill=0;
var usrcount=0;
var pwdcount=0;
var fnamecount=0;
var lnamecount=0;
var filecount=0;
var dobcount=0;
var hobcount=0;
var countrycount=0;
var phcount=0;

// User Name Validation
function username_validation()
{
	
	var user=document.getElementById('uname').value;
	var patt1=/^[a-z A-Z 0-9]{5,8}$/;
	var ulen=user.match(patt1);
	
	if(ulen==null || ulen=='')
	{
		document.getElementById('emsg').innerHTML =" Required and must be of length 5 to 8"
		//uname.focus();
		return false;
		
	}
	else
	{
		if(usrcount<=0)	
		fill=fill+temp1+0.000000001;
		usrcount++;
		document.getElementById('emsg').innerHTML = "";
		return true;	
		
	}
}

function password_validation()
{
	var pwd=document.getElementById('pwd').value;
	var patt1=/^[a-z A-Z 0-9]{1,6}$/;
	var plen=pwd.match(patt1);

	if(plen==null || plen=='')
	{
		document.getElementById('pwdemsg').innerHTML =" Required and must be of Maximum length 6"
		
		
		//pwd.focus();
		return false;
	}
	else
	{
		if(pwdcount<=0)
		fill=fill+temp1;
		pwdcount++;
		document.getElementById('pwdemsg').innerHTML = "";
		return true;
	}
}//password_validation()

//First Name Validation
function fname_validation()
{
	var fnamelength=document.getElementById('fname').value.length;
	
	if(fnamelength<2 || fnamelength>6)
	{
		
		document.getElementById('fnameemsg').innerHTML =" Required and must be of length 2 to 6 "
		//fname.focus();
		
		return false;
	}
	else
	{
		if(fnamecount<=0)
		fill=fill+temp1;
		fnamecount++;
		document.getElementById('fnameemsg').innerHTML = "";
		
		return true;
	}
}//fname_validation()


//Last Name Validation

function lname_validation()
{

	var lnamelength=document.getElementById('lname').value.length;


	if(lnamelength<2 || lnamelength>15)
	{
		
		document.getElementById('lnameemsg').innerHTML =" Required and must be of length 2 to 15"
		//lname.focus();
		
		return false;
	}
	else
	{
		 
		if(lnamecount<=0)
		fill=fill+temp1;
		lnamecount++;
		document.getElementById('lnameemsg').innerHTML = "";
		
		return true;
	}

}//lname_validation()


//File Upload Validation	

function fileupload_validation()
{
var fileName =document.getElementById('pic').value;

var ext = fileName.substring(fileName.lastIndexOf('.') + 1);
if(ext == "gif" || ext == "GIF" || ext == "JPG" || ext == "jpg" || ext == "png" || ext == "PNG")
{
document.getElementById('picemsg').innerHTML = "";

		if(filecount<=0)
		fill=fill+temp1;
		filecount++;
return true;

} 
else
{
document.getElementById('picemsg').innerHTML = "<span style='color:red;font-size:12'>Upload Only .gif/.jpg/.png Only</span>"
 
		
return false;
}
}//fileupload_validation()


//Date of Birth Validation

function dob_validation()
{
var dayindex=document.getElementById("daysel").selectedIndex;
var monthindex=document.getElementById("monthsel").selectedIndex;
var yearindex=document.getElementById("yearsel").selectedIndex;
	
	if(dayindex==0 || monthindex==0 || yearindex==0)
	{
		
		document.getElementById('dobemsg').innerHTML = "Required"
		//daysel.focus();
		return false;
	}
	else
	{
		 
		if(dobcount<=0)
		fill=fill+temp1;
		dobcount++;
		document.getElementById('dobemsg').innerHTML = ""
		return true;
	}
}//dob_validation()

//Country Select Box Validation

function countryselect_validation()
{

var index=document.getElementById("countries").selectedIndex;
	
	if(index<0)
	{
		document.getElementById('countryemsg').innerHTML = " Required"
		//countries.focus();
		return false;
	}
	else
	{
		 
		if(countrycount<=0)
		fill=fill+temp1;
		countrycount++;
		document.getElementById('countryemsg').innerHTML = ""
		return true;
	}
}//countryselect_validation()


//Phone Number Validation

function phonenumber_validation()
{
	var phno=document.getElementById("phno1").value;
//	var patt1=/^\+91\(?([0-9]{3})\)?[\)]?\)[-. ]?([0-9]{3})[-. ]?([0-9]{4})$/;  
	
var patt1=/^\+\s[9{1}][]?[1{1}]\s ?[\)]?\([]?([0-9]{3})\)?[\)]?\)[]?[\)]?\-[]?([0-9]{3})?[\)]?\-[]?([0-9]{4})$/;
	if(phno.match(patt1))
	{
		 
		if(phcount<=0)
		fill=fill+temp1;
		phcount++;
		document.getElementById('phnoemsg').innerHTML = "";
		return true;	
	}	
	else
	{
		document.getElementById('phnoemsg').innerHTML = "<span style='color:red;font-size:12'>Format Should Be + 91 (953)-305-8651)</span>"
		return false;
	}
}//phonenumber_validation()

// Radio Button Validation

function radio_validation()
{
var radios = document.getElementsByName("hob");
    var formValid = false;
    var inc = 0;

    while (!formValid && inc < radios.length) {

        if (radios[inc].checked)
		 formValid = true;
	         inc++;        
    }

    if (!formValid) 
	{

		document.getElementById('hobemsg').innerHTML = " Required"
		return false; temp=0;
	}
	else
	{	
		 
		if(hobcount<=0)
		fill=fill+temp1;
		hobcount++;
		temp=1;
		document.getElementById('hobemsg').innerHTML = " "
		return true;  
	}

}//radio_validation()




function validateForm(myform)
{
	
		username_validation();
		password_validation();
		fname_validation();
		lname_validation();
		fileupload_validation();
		dob_validation();
		countryselect_validation();
		phonenumber_validation();
		radio_validation();
		prograssBar();
		targetGroup();
	
return false;
}

function targetGroup(){

    var elemArray = document.getElementsByClassName('esp');
	var flag=0;
    for(var i = 0; i < elemArray.length; i++){
	var elem = document.getElementById(elemArray[i].id);
		var value=elem.innerHTML;

		if(value.length==0)
		{	flag++;  }
					
			if(flag==8 && temp==1 ) {
				msgBox();
			}
			else {
			var elem = document.getElementById("msgbox");
			elem.style.display="none";
			}
    }

return false;
}

function msgBox()
{
var elem = document.getElementById("msgbox");
	elem.style.display="block";
	return false;
}//MmsgBox()

//progressbar
function prograssBar()
{
	var pgbar = document.getElementById("progressbar");
	pgbar.style.width=fill+'%';
	document.getElementById("percent").innerHTML=fill+'% Filled';
}

