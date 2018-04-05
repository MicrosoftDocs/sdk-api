---
UID: NF:winspool.GetJobA
title: GetJobA function
author: windows-driver-content
description: The GetJob function retrieves information about a specified print job.
old-location: gdi\getjob.htm
old-project: printdocs
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetJob, GetJob function [Windows GDI], GetJobA, GetJobW, _win32_GetJob, gdi.getjob, winspool/GetJob, winspool/GetJobA, winspool/GetJobW
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
req.unicode-ansi: GetJobW (Unicode) and GetJobA (ANSI)
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
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	GetJob
-	GetJobA
-	GetJobW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetJobA function


## -description


The <b>GetJob</b> function retrieves information about a specified print job.


## -parameters




### -param hPrinter [in]

A handle to the printer for which the print-job data is retrieved. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param JobId [in]

Identifies the print job for which to retrieve data. Use the <a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a> function or <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> function to get a print job identifier.


### -param Level [in]

The type of information returned in the <i>pJob</i> buffer. If <i>Level</i> is 1, <i>pJob</i> receives a <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a> structure. If <i>Level</i> is 2, <i>pJob</i> receives a <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a> structure.


### -param pJob [out]

A pointer to a buffer that receives a <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a> or a <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a> structure containing information about the job. The buffer must be large enough to store the strings pointed to by the structure members.

To determine the required buffer size, call <b>GetJob</b> with <i>cbBuf</i> set to zero. <b>GetJob</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


### -param cbBuf [in]

The size, in bytes, of the array.


### -param pcbNeeded [out]

A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if <i>cbBuf</i> is too small.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a>



<a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>



<a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/a103a29c-be4d-491e-9b04-84571fe969a5">ScheduleJob</a>



<a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a>
 

 

