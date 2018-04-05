---
UID: NF:winspool.FreePrinterNotifyInfo
title: FreePrinterNotifyInfo function
author: windows-driver-content
description: The FreePrinterNotifyInfo function frees a system-allocated buffer created by the FindNextPrinterChangeNotification function.
old-location: gdi\freeprinternotifyinfo.htm
old-project: printdocs
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FreePrinterNotifyInfo, FreePrinterNotifyInfo function [Windows GDI], _win32_FreePrinterNotifyInfo, gdi.freeprinternotifyinfo, winspool/FreePrinterNotifyInfo
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
-	FreePrinterNotifyInfo
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# FreePrinterNotifyInfo function


## -description


The <b>FreePrinterNotifyInfo</b> function frees a system-allocated buffer created by the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function.


## -parameters




### -param pPrinterNotifyInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/c104fabe-edf5-426e-859b-694811975623">PRINTER_NOTIFY_INFO</a> buffer returned from a call to the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function. <b>FreePrinterNotifyInfo</b> deallocates this buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/c104fabe-edf5-426e-859b-694811975623">PRINTER_NOTIFY_INFO</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

