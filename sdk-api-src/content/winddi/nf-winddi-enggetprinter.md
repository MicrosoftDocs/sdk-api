---
UID: NF:winddi.EngGetPrinter
title: EngGetPrinter function
author: windows-sdk-content
description: The EngGetPrinter function retrieves information about the specified printer.
old-location: display\enggetprinter.htm
tech.root: display
ms.assetid: dd492777-48a2-4fb6-9202-a2af3b632678
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngGetPrinter, EngGetPrinter function [Display Devices], display.enggetprinter, gdifncs_6e95ce51-f1ca-4e44-b26d-b677ace5e297.xml, winddi/EngGetPrinter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngGetPrinter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngGetPrinter function


## -description


The <b>EngGetPrinter</b> function retrieves information about the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which data should be retrieved. This is the handle that is passed as the <i>hDriver</i> parameter of <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>.


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



<b>EngGetPrinter</b> returns <b>TRUE</b> upon success; otherwise, it logs an error and returns <b>FALSE</b>. To get error information, call <a href="https://msdn.microsoft.com/47138077-125e-4da9-b0de-e437a9b1733d">EngGetLastError</a>.




## -remarks



The PRINTER_INFO_<i>X</i> structures are defined in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>
 

 

