1. To work with radio button and div tage

function setObject(){
	var obj=document.getElementById("Object").value;
	var no=trobj.indexOf("WiFi");
	if(no>=1){
		//alert("wifi");
		$('#divnetwork').show();   //show div
		//var netval=$('input[name="network"]:checked').val();
		//frmdevicetype.parameterName.value=obj+netval;
	}else{
		frmdevicetype.parameterName.value=obj;
		$('#divnetwork').hide();
		
	}
	
	$(document).ready(function(){
		$("input[name=network]:radio").change(function(){    //event to list radion button change
			//alert('did it');
			var netval=$('input[name="network"]:checked').val();  //to get the radion button checked value
			frmdevicetype.parameterName.value=obj+netval;
		});
	});
	
}
</script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.2/jquery.min.js"></script>
//div should be inside <td> not <tr>
<td>
									<div id="divnetwork" name="divnetwork" style="display:none";>
									A<input name="network" type="radio" value="10."/>&nbsp;&nbsp;&nbsp; 
									B<input name="network" type="radio" value="20." />&nbsp;&nbsp;&nbsp; 
									C<input checked="checked" name="network" type="radio" value="30." />
									</div>
</td>
