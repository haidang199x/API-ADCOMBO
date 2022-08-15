<?
//Data to send
$name = $_POST['name'];
$phone = $_POST['phone'];
$offer_id = '31066'; //Offer ID
$api_key = '6ec5da7c37c82704114b58b29cfc77b8'; //API key
$country_code = 'RS'; //Geo
$base_url = 'land1.abxyz.info'; //Link to landing page
$price = '3700'; //Product price
$referrer = 'vk.com'; //Link to the landing page from which you are uploading
$ip = $_SERVER['REMOTE_ADDR'];

$params = array(

'api_key' => $api_key,
'name' => $name,
'phone' => $phone,
'offer_id' => $offer_id,
'country_code' => $country_code,
'base_url' => $base_url,
'price ' => $price,
'referrer' => $referrer,
'ip' => $ip

);

if($curl = curl_init()){

curl_setopt($curl, CURLOPT_URL, 'https://api.adcombo.com/api/v2/order/create/?'.http_build_query($params));
curl_setopt($curl, CURLOPT_RETURNTRANSFER,true);
$resp = curl_exec($curl);
curl_close($curl);

}

header('Location: success.html');
