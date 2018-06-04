---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EngGetPrinter function


## -description


The <b>EngGetPrinter</b> function retrieves information about the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which data should be retrieved. This is the handle that is passed as the <i>hDriver</i> parameter of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param dwLevel [in]

Specifies the version of the structure to which <i>pPrinter</i> points. This parameter can have any of the following values:

<table>
<tr>
<th>Value</th>
<th>Structure Returned via <i>pPrinter</i></th>
</tr>
<tr>
<td>
1

</td>
<td>
PRINTER_INFO_1

</td>
</tr>
<tr>
<td>
2

</td>
<td>
PRINTER_INFO_2

</td>
</tr>
<tr>
<td>
3

</td>
<td>
PRINTER_INFO_3

</td>
</tr>
<tr>
<td>
4

</td>
<td>
PRINTER_INFO_4

</td>
</tr>
<tr>
<td>
5

</td>
<td>
PRINTER_INFO_5

</td>
</tr>
</table>
 


### -param pPrinter [out, optional]

Pointer to the memory buffer in which the printer information structure, identified by <i>dwLevel</i>, is loaded.


### -param cbBuf [in]

Specifies the size, in bytes, of the memory buffer pointed to by <i>pPrinter</i>.


### -param pcbNeeded [out]

Pointer to a memory location that receives the number of bytes copied if the function succeeds, or the number of required bytes if <i>cbBuf</i> is too small.


## -returns



<b>EngGetPrinter</b> returns <b>TRUE</b> upon success; otherwise, it logs an error and returns <b>FALSE</b>. To get error information, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>.




## -remarks



The PRINTER_INFO_<i>X</i> structures are defined in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>
 

 

