<div align="center">

## A Simple Hit Counter


</div>

### Description

This is just a simple hits counter that will display the following:

hits: 345

or whatever the file says

chmod "counter.txt" to 0777 for this to work
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jeff Cook/Moab Software](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jeff-cook-moab-software.md)
**Level**          |Beginner
**User Rating**    |4.5 (36 globes from 8 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__8-9.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jeff-cook-moab-software-a-simple-hit-counter__8-1008/archive/master.zip)





### Source Code

```
<?php
$file="counter.txt";
$handle=fopen($file, "r+");
$hits=fread($handle,filesize("$file"));
$hits+=1;
fclose($handle);
echo "$hits";
$handle=fopen($file, "w");
fwrite($handle, $hits);
fclose($handle);
 ?>
```

