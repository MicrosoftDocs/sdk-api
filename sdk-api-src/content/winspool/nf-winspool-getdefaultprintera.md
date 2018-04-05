---
UID: NF:winspool.GetDefaultPrinterA
title: GetDefaultPrinterA function
author: windows-driver-content
description: The GetDefaultPrinter function retrieves the printer name of the default printer for the current user on the local computer.
old-location: gdi\getdefaultprinter.htm
old-project: printdocs
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetDefaultPrinter, GetDefaultPrinter function [Windows GDI], GetDefaultPrinterA, GetDefaultPrinterW, _win32_GetDefaultPrinter, gdi.getdefaultprinter, winspool/GetDefaultPrinter, winspool/GetDefaultPrinterA, winspool/GetDefaultPrinterW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDefaultPrinterW (Unicode) and GetDefaultPrinterA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winspool.drv
api_name:
-	GetDefaultPrinter
-	GetDefaultPrinterA
-	GetDefaultPrinterW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetDefaultPrinterA function


## -description


The <b>GetDefaultPrinter</b> function retrieves the printer name of the default printer for the current user on the local computer.


## -parameters




### -param pszBuffer [in]

A pointer to a buffer that receives a null-terminated character string containing the default printer name. If this parameter is <b>NULL</b>, the function fails and the variable pointed to by <i>pcchBuffer</i> returns the required buffer size, in characters.


### -param pcchBuffer [in, out]

On input, specifies the size, in characters, of the <i>pszBuffer</i> buffer. On output, receives the size, in characters, of the printer name string, including the terminating null character.


## -returns



If the function succeeds, the return value is a nonzero value and the variable pointed to by <i>pcchBuffer</i> contains the number of characters copied to the <i>pszBuffer</i> buffer, including the terminating null character.

If the function fails, the return value is zero. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ERROR_INSUFFICIENT_BUFFER</td>
<td>The <i>pszBuffer</i> buffer is too small. The variable pointed to by <i>pcchBuffer</i> contains the required buffer size, in characters.</td>
</tr>
<tr>
<td>ERROR_FILE_NOT_FOUND</td>
<td>There is no default printer.</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/55eec548-577f-422b-80e3-8b23aa4d2159">SetDefaultPrinter</a>
 

 

