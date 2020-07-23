# dynamic
dynamaic website
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    
    <style>
        * {margin: 0;padding: 0;border: 0;
            box-sizing: border-box
        }
        ul, li {list-style: none}
        a {color: inherit}
        p {width: 200px;height: 50px;
            border: 1px solid #f00
        }
		
		dl{position: relative}
        dt{ width: 100px;height: 50px;
            border: 1px solid #f00;
            position: absolute; top: 0;
        }
        dt:nth-of-type(1){left: 0;}
        dt:nth-of-type(2){left: 100px;}
        dt:nth-of-type(3){left: 200px;}
        dd{width: 300px; height: 200px;
            border: 1px solid #00f;
            background-color: #fff;
            position: absolute; left: 0; top: 50px;
        }
	  dd:nth-of-type(1){z-index: 100;}

    </style>
    
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
    <script>
        $(function(){
			$('dt').on('click',function(){
				$('dd').slideUp(); 
				$(this).next().slideDown();
			})
        })
    </script>
    
    
</head>
<body>
    <dl>
        <dt>메뉴1</dt>
        <dd>내용111111</dd>
        <dt>메뉴2</dt>
        <dd>내용222222</dd>
        <dt>메뉴3</dt>
        <dd>내용333333</dd>
    </dl>

</body>

</html>
