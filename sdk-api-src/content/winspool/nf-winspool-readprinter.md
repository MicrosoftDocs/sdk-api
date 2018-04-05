---
UID: NF:winspool.ReadPrinter
title: ReadPrinter function
author: windows-driver-content
description: The ReadPrinter function retrieves data from the specified printer.
old-location: gdi\readprinter.htm
old-project: printdocs
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ReadPrinter, ReadPrinter function [Windows GDI], _win32_ReadPrinter, gdi.readprinter, winspool/ReadPrinter
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
-	ReadPrinter
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ReadPrinter function


## -description


The <b>ReadPrinter</b> function retrieves data from the specified printer.


## -parameters




### -param hPrinter [in]

A handle to the printer object for which to retrieve data. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> function to retrieve a printer object handle. Use the format: Printername, Job xxxx.


### -param pBuf [out]

A pointer to a buffer that receives the printer data.


### -param cbBuf [in]

The size, in bytes, of the buffer to which <i>pBuf</i> points.


### -param pNoBytesRead [out]

A pointer to a variable that receives the number of bytes of data copied into the array to which <i>pBuf</i> points.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<b>ReadPrinter</b> returns an error if the device or the printer is not bidirectional.




## -see-also




<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

