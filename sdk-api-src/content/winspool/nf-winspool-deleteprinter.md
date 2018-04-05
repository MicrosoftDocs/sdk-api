---
UID: NF:winspool.DeletePrinter
title: DeletePrinter function
author: windows-driver-content
description: The DeletePrinter function deletes the specified printer object.
old-location: gdi\deleteprinter.htm
old-project: printdocs
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePrinter, DeletePrinter function [Windows GDI], _win32_DeletePrinter, gdi.deleteprinter, winspool/DeletePrinter
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
-	Spoolss.dll
api_name:
-	DeletePrinter
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinter function


## -description


The <b>DeletePrinter</b> function deletes the specified printer object.


## -parameters




### -param hPrinter [in, out]

Handle to a printer object that will be deleted. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
If there are print jobs remaining to be processed for the specified printer, <b>DeletePrinter</b> marks the printer for pending deletion, and then deletes it when all the print jobs have been printed. No print jobs can be added to a printer that is marked for pending deletion.

A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted. If the printer is held and there are jobs for the printer, <b>DeletePrinter</b> fails with ERROR_ACCESS_DENIED.

Note that <b>DeletePrinter</b> does not close the handle that is passed to it. Thus, the application must still call <a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>.




## -see-also




<a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>



<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

