---
UID: NF:winspool.DeletePrinterKeyW
title: DeletePrinterKeyW function
author: windows-driver-content
description: The DeletePrinterKey function deletes a specified key and all its subkeys for a specified printer.
old-location: gdi\deleteprinterkey.htm
old-project: printdocs
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrinterKey, DeletePrinterKey function [Windows GDI], DeletePrinterKeyA, DeletePrinterKeyW, _win32_DeletePrinterKey, gdi.deleteprinterkey, winspool/DeletePrinterKey, winspool/DeletePrinterKeyA, winspool/DeletePrinterKeyW
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
req.unicode-ansi: DeletePrinterKeyW (Unicode) and DeletePrinterKeyA (ANSI)
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
-	DeletePrinterKey
-	DeletePrinterKeyA
-	DeletePrinterKeyW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinterKeyW function


## -description


The <b>DeletePrinterKey</b> function deletes a specified key and all its subkeys for a specified printer.


## -parameters




### -param hPrinter [in]

A handle to the printer for which the function deletes a key. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pKeyName [in]

A pointer to a null-terminated string that specifies the key to delete. Use the backslash ( \ ) character as a delimiter to specify a path with one or more subkeys.

If <i>pKeyName</i> is an empty string (""), <b>DeletePrinterKey</b> deletes all keys below the top-level key for the printer. If <i>pKeyName</i> is <b>NULL</b>, <b>DeletePrinterKey</b> returns ERROR_INVALID_PARAMETER.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a system error code.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55">DeletePrinterDataEx</a>



<a href="https://msdn.microsoft.com/bc5ecc46-24a4-4b54-9431-0eaf6446e2d6">EnumPrinterDataEx</a>



<a href="https://msdn.microsoft.com/721b1d23-a594-4439-b8f9-9b11be5fe874">EnumPrinterKey</a>



<a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a>
 

 

