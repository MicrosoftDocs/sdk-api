---
UID: NF:winspool.GetPrintExecutionData
title: GetPrintExecutionData function
author: windows-driver-content
description: The GetPrintExecutionData retrieves the current print context.
old-location: gdi\getprintexecutiondata.htm
old-project: printdocs
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetPrintExecutionData, GetPrintExecutionData function [Windows GDI], gdi.getprintexecutiondata, winspool/GetPrintExecutionData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
-	winspool.drv
api_name:
-	GetPrintExecutionData
product: Windows
targetos: Windows
req.lib: 
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPrintExecutionData function


## -description


The <b>GetPrintExecutionData</b> retrieves the current print context.


<div class="alert"><b>Note</b>  This function is intended for use by printer drivers that are running in the context of the print spooler.</div>
<div> </div>



## -parameters




### -param pData [out]

A pointer to a variable that receives the address of the <a href="https://msdn.microsoft.com/1fd25ed9-6f28-48f9-8132-d48fffc956ec">PRINT_EXECUTION_DATA</a> structure.


## -returns



Returns <b>TRUE</b> if the function succeeds; otherwise <b>FALSE</b>. If the return value is <b>FALSE</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get the error status.




## -remarks



Printer drivers should call  <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> on the winspool.drv module to get the address of the <b>GetPrintExecutionData</b> function because <b>GetPrintExecutionData</b> is not supported on Windows Vista or earlier versions of Windows.

<b>GetPrintExecutionData</b> only  fails if the value of <i>pData</i> is <b>NULL</b>.

The value of the <b>clientAppPID</b> member of <a href="https://msdn.microsoft.com/1fd25ed9-6f28-48f9-8132-d48fffc956ec">PRINT_EXECUTION_DATA</a> is only meaningful if the value of  <b>context</b> is <b>PRINT_EXECUTION_CONTEXT_WOW64</b>. If the value of <b>context</b> is not <b>PRINT_EXECUTION_CONTEXT_WOW64</b>, the value of <b>clientAppPID</b> is 0.




## -see-also




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/b6c026b2-8519-45d3-9614-b502eec23cde">PRINT_EXECUTION_CONTEXT</a>



<a href="https://msdn.microsoft.com/1fd25ed9-6f28-48f9-8132-d48fffc956ec">PRINT_EXECUTION_DATA</a>
 

 

