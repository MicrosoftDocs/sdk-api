---
UID: NF:winspool.EnumJobsA
title: EnumJobsA function
author: windows-driver-content
description: The EnumJobs function retrieves information about a specified set of print jobs for a specified printer.
old-location: gdi\enumjobs.htm
old-project: printdocs
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 1, 2, 3, EnumJobs, EnumJobs function [Windows GDI], EnumJobsA, EnumJobsW, _win32_EnumJobs, gdi.enumjobs, winspool/EnumJobs, winspool/EnumJobsA, winspool/EnumJobsW
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
req.unicode-ansi: EnumJobsW (Unicode) and EnumJobsA (ANSI)
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
-	EnumJobs
-	EnumJobsA
-	EnumJobsW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumJobsA function


## -description


The <b>EnumJobs</b> function retrieves information about a specified set of print jobs for a specified printer.


## -parameters




### -param hPrinter [in]

A handle to the printer object whose print jobs the function enumerates. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param FirstJob [in]

The zero-based position within the print queue of the first print job to enumerate. For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.


### -param NoJobs [in]

The total number of print jobs to enumerate.


### -param Level [in]

The type of information returned in the <i>pJob</i> buffer.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
<i>pJob</i> receives an array of <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a> structures

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
<i>pJob</i> receives an array of <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a> structures

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
<i>pJob</i> receives an array of <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> structures

</td>
</tr>
</table>
 


### -param pJob [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>, <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>, or <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> structures. The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.

To determine the required buffer size, call <b>EnumJobs</b> with <i>cbBuf</i> set to zero. <b>EnumJobs</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


### -param cbBuf [in]

The size, in bytes, of the <i>pJob</i> buffer.


### -param pcbNeeded [out]

A pointer to a variable that receives the number of bytes copied if the function succeeds. If the function fails, the variable receives the number of bytes required.


### -param pcReturned [out]

A pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>, <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>, or <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> structures returned in the <i>pJob</i> buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a> structure contains general print-job information; the <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a> structure has much more detailed information. The <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> structure contains information about how jobs are linked.

To determine the number of print jobs in the printer queue, call the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function with the <i>Level</i> parameter set to 2.




## -see-also




<a href="https://msdn.microsoft.com/57e59f84-d2a0-4722-b0fc-6673f7bb5c57">GetJob</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>



<a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>



<a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a>
 

 

