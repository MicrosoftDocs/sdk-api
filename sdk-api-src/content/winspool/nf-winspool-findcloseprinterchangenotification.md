---
UID: NF:winspool.FindClosePrinterChangeNotification
title: FindClosePrinterChangeNotification function
author: windows-driver-content
description: The FindClosePrinterChangeNotification function closes a change notification object created by calling the FindFirstPrinterChangeNotification function.
old-location: gdi\findcloseprinterchangenotification.htm
old-project: printdocs
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FindClosePrinterChangeNotification, FindClosePrinterChangeNotification function [Windows GDI], _win32_FindClosePrinterChangeNotification, gdi.findcloseprinterchangenotification, winspool/FindClosePrinterChangeNotification
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
-	FindClosePrinterChangeNotification
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# FindClosePrinterChangeNotification function


## -description


The <b>FindClosePrinterChangeNotification</b> function closes a change notification object created by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> function. The printer or print server associated with the change notification object will no longer be monitored by that object.


## -parameters




### -param hChange [in]

A handle to the change notification object to be closed. This is a handle created by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> function.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
After calling the <b>FindClosePrinterChangeNotification</b> function, you cannot use the <i>hChange</i> handle in subsequent calls to either <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> or <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

