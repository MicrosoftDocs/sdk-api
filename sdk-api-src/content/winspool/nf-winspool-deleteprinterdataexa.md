---
UID: NF:winspool.DeletePrinterDataExA
title: DeletePrinterDataExA function
author: windows-driver-content
description: The DeletePrinterDataEx function deletes a specified value from the configuration data for a printer.
old-location: gdi\deleteprinterdataex.htm
old-project: printdocs
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrinterDataEx, DeletePrinterDataEx function [Windows GDI], DeletePrinterDataExA, DeletePrinterDataExW, _win32_DeletePrinterDataEx, gdi.deleteprinterdataex, winspool/DeletePrinterDataEx, winspool/DeletePrinterDataExA, winspool/DeletePrinterDataExW
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
req.unicode-ansi: DeletePrinterDataExW (Unicode) and DeletePrinterDataExA (ANSI)
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
-	Ext-MS-Win-printer-Winspool-l1-1-1.dll
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	DeletePrinterDataEx
-	DeletePrinterDataExA
-	DeletePrinterDataExW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinterDataExA function


## -description


The <b>DeletePrinterDataEx</b> function deletes a specified value from the configuration data for a printer. A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys. The function deletes a specified value under a specified key.

Like the <a href="https://msdn.microsoft.com/03c0bd75-d6de-46e3-b8e9-5a55df5135ea">DeletePrinterData</a> function, <b>DeletePrinterDataEx</b> can delete values stored by the <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a> function. In addition, <b>DeletePrinterDataEx</b> can delete values stored under a specified key by the <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> function.


## -parameters




### -param hPrinter [in]

A handle to the printer for which the function deletes a value. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pKeyName [in]

A pointer to a null-terminated string that specifies the key containing the value to delete. Use the backslash ( \ ) character as a delimiter to specify a path that has one or more subkeys.

If <i>pKeyName</i> is <b>NULL</b> or an empty string, <b>DeletePrinterDataEx</b> returns ERROR_INVALID_PARAMETER.


### -param pValueName [in]

A pointer to a null-terminated string that specifies the name of the value to delete.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a system error code.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0bd81b43-5c1e-4989-8350-2ec0dc215f28">DeletePrinterKey</a>



<a href="https://msdn.microsoft.com/bc5ecc46-24a4-4b54-9431-0eaf6446e2d6">EnumPrinterDataEx</a>



<a href="https://msdn.microsoft.com/721b1d23-a594-4439-b8f9-9b11be5fe874">EnumPrinterKey</a>



<a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a>
 

 

