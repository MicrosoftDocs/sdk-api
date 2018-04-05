---
UID: NF:winspool.FlushPrinter
title: FlushPrinter function
author: windows-driver-content
description: The FlushPrinter function sends a buffer to the printer in order to clear it from a transient state.
old-location: gdi\flushprinter.htm
old-project: printdocs
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FlushPrinter, FlushPrinter function [Windows GDI], _win32_FlushPrinter, gdi.flushprinter, winspool/FlushPrinter
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
-	Winspool.drv
api_name:
-	FlushPrinter
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# FlushPrinter function


## -description


The <b>FlushPrinter</b> function sends a buffer to the printer in order to clear it from a transient state.


## -parameters




### -param hPrinter [in]

A handle to the printer object. This should be the same handle that was used, in a prior <a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a> call, by the printer driver.


### -param pBuf [in]

A pointer to an array of bytes that contains the data to be written to the printer.


### -param cbBuf [in]

The size, in bytes, of the array pointed to by <i>pBuf</i>.


### -param pcWritten [out]

A pointer to a value that receives the number of bytes of data that were written to the printer.


### -param cSleep [in]

The time, in milliseconds, for which the I/O line to the printer port should be kept idle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<b>FlushPrinter</b> should be called only if <a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a> failed, leaving the printer in a transient state. For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.

<b>FlushPrinter</b> also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.




## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>
 

 

