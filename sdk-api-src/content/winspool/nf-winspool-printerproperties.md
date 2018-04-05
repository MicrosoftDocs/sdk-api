---
UID: NF:winspool.PrinterProperties
title: PrinterProperties function
author: windows-driver-content
description: The PrinterProperties function displays a printer-properties property sheet for the specified printer.
old-location: gdi\printerproperties.htm
old-project: printdocs
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PrinterProperties, PrinterProperties function [Windows GDI], _win32_PrinterProperties, gdi.printerproperties, winspool/PrinterProperties
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
req.unicode-ansi: 
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
-	plotui.dll
api_name:
-	PrinterProperties
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Plotui.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PrinterProperties function


## -description


The <b>PrinterProperties</b> function displays a printer-properties property sheet for the specified printer.


## -parameters




### -param hWnd [in]

A handle to the parent window of the property sheet.


### -param hPrinter [in]

A handle to a printer object. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

