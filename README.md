Signgen
=======

Forked from `devcookies/signgen` due it's removal from github.

Signature generator for various devcookies software API

PHP
---

Supported version: 5.3+

Code example:

	<?php
	require_once "path/to/php/devcookies/SignatureGenerator.php";
	
	$generator = new devcookies\SignatureGenerator("my_salt_from_manager");

	$requestParams = array(
		"site_id" => 100239,
		"action" => "createorder",
		"...",
	);
	
	$requestParams["signature"] = $generator->assemble($requestParams);

