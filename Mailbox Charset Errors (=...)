<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

	<?php
ini_set ('max_execution_time', 0);
				$hatali=array(
				"=E7","=C7",
				"=FD","=DD",
				"=FC","=DC",
				"=F6","=D6",
				"=FE","=DE",
				"=F0","=D0",
				"=20",
				"=C4=9E","=C4=9F",
				"=C4=B0","=C4=B1",
				"=C3=BC","=C3=9C",
				"=C5=9F","=C5=9E",
				"=C3=B6","=C3=96",
				"=C3=87","=C3=A7",
				"Ä","Ä?",
				"Ä°","Ä±",
				"Ã?","Ã¶",
				"Å","Å?",
				"Ã?","Ã¼",
				"=\r\n",
				"=E2=80=99"
				);
				$duzgun=array(
				"ç","Ç",
				"ı","İ",
				"ü","Ü",
				"ö","Ö",
				"ş","Ş",
				"ğ","Ğ",
				"\r\n",
				"Ğ","ğ",
				"İ","ı",
				"ü","Ü",
				"ş","Ş",
				"ö","Ö",
				"Ç","ç",
				"Ğ","ğ",
				"İ","ı",
				"Ö","ö",
				"Ş","ş",
				"Ü","ü",
				"",
				"\'"
				);

		
		$mailbox = imap_open('{imap-mail.outlook.com:993/ssl}',"mail@hotm.","password"); 
		$check=imap_check($mailbox);
		$bodyText =imap_fetchbody($mailbox,1,1.2);
    
		for ($i=0; $i<$check->Nmsgs ; $i++) 
		{ 
			for ($t=0; $t <count($hatali) ; $t++) 
			{ 
				$aranan = strpos($bodyText,$hatali[$t]);
				if ($aranan!==false) 
				{
					$bodyText=str_replace($hatali[$t], $duzgun[$t],$bodyText);
				}
			}
		}
		echo($bodyText);
	 ?>
</body>
</html>
