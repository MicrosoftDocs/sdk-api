---
UID: NF:winspool.ResetPrinterA
title: ResetPrinterA function
author: windows-driver-content
description: The ResetPrinter function specifies the data type and device mode values to be used for printing documents submitted by the StartDocPrinter function. These values can be overridden by using the SetJob function after document printing has started.
old-location: gdi\resetprinter.htm
old-project: printdocs
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ResetPrinter, ResetPrinter function [Windows GDI], ResetPrinterA, ResetPrinterW, _win32_ResetPrinter, gdi.resetprinter, winspool/ResetPrinter, winspool/ResetPrinterA, winspool/ResetPrinterW
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
req.unicode-ansi: ResetPrinterW (Unicode) and ResetPrinterA (ANSI)
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
-	ResetPrinter
-	ResetPrinterA
-	ResetPrinterW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ResetPrinterA function


## -description


The <b>ResetPrinter</b> function specifies the data type and device mode values to be used for printing documents submitted by the <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a> function. These values can be overridden by using the <a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a> function after document printing has started.


## -parameters




### -param hPrinter [in]

Handle to the printer. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pDefault [in]

Pointer to a <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure.

The <b>ResetPrinter</b> function ignores the <b>DesiredAccess</b> member of the <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure. Set that member to zero.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>
 

 

