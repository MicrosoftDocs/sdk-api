---
UID: NF:winspool.SetDefaultPrinterW
title: SetDefaultPrinterW function
author: windows-driver-content
description: The SetDefaultPrinter function sets the printer name of the default printer for the current user on the local computer.
old-location: gdi\setdefaultprinter.htm
old-project: printdocs
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetDefaultPrinter, SetDefaultPrinter function [Windows GDI], SetDefaultPrinterA, SetDefaultPrinterW, _win32_SetDefaultPrinter, gdi.setdefaultprinter, winspool/SetDefaultPrinter, winspool/SetDefaultPrinterA, winspool/SetDefaultPrinterW
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
req.unicode-ansi: SetDefaultPrinterW (Unicode) and SetDefaultPrinterA (ANSI)
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
-	SetDefaultPrinter
-	SetDefaultPrinterA
-	SetDefaultPrinterW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetDefaultPrinterW function


## -description


The <b>SetDefaultPrinter</b> function sets the printer name of the default printer for the current user on the local computer.


## -parameters




### -param pszPrinter [in]

A pointer to a null-terminated string containing the default printer name. For a remote printer connection, the name format is <b>\\</b><i>server</i><b>\</b><i>printername</i>. For a local printer, the name format is <i>printername</i>.

If this parameter is <b>NULL</b> or an empty string, that is, "", <b>SetDefaultPrinter</b> will select a default printer from one of the installed printers. If a default printer already exists, calling <b>SetDefaultPrinter</b> with a <b>NULL</b> or an empty string  in this parameter might change the default printer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



When using this method, you must specify a valid printer, driver, and port. If they are invalid, the APIs do not fail but the result is not defined. This could cause other programs to set the printer back to the previous valid printer. You can use <a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a> to retrieve the printer name, driver name, and port name of all available printers.

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/8ec06743-43ce-4fac-83c4-f09eac7ee333">GetDefaultPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

