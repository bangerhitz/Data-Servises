<?php
// Read the variables sent via POST from our API
$sessionId   = $_POST["sessionId"];
$serviceCode = $_POST["serviceCode"];
$phoneNumber = $_POST["phoneNumber"];
$text        = $_POST["text"];

if ($text == "") {
    // This is the first request. Note how we start the response with CON
    $response  = "CON Choose your data plan \n";
    $response .= "1. MTN DATA\n";
    $response .= "2. AT DATA ";
    $response .="3. TELECEL DATA";

} else if ($text == "1") {
    // Business logic for first level response
    $response = "CON Select your data plan \n";
    $response .= "1. 1gb--GH₵7.00 \n";

} else if ($text == "2") {
    // Business logic for first level response
    // This is a terminal request. Note how we start the response with CON
    $response = "CON Payment Method ".$1. Mobile Money;
   
} else if($text == "1*1") { 
    // This is a second level response where the user selected 1 in the first instance
    $MTN DATA = "NOT AVAILABLE";

    // This is a terminal request. Note how we start the response with END
    $response = "END TRY AGAING LATER ".$MTN DATA;

}

// Echo the response back to the API
header('Content-type: text/plain');
echo $response;
