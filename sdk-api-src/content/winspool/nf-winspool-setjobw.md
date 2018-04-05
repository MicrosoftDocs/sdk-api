---
UID: NF:winspool.SetJobW
title: SetJobW function
author: windows-driver-content
description: The SetJob function pauses, resumes, cancels, or restarts a print job on a specified printer. You can also use the SetJob function to set print job parameters, such as the print job priority and the document name.
old-location: gdi\setjob.htm
old-project: printdocs
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: JOB_CONTROL_CANCEL, JOB_CONTROL_DELETE, JOB_CONTROL_LAST_PAGE_EJECTED, JOB_CONTROL_PAUSE, JOB_CONTROL_RELEASE, JOB_CONTROL_RESTART, JOB_CONTROL_RESUME, JOB_CONTROL_RETAIN, JOB_CONTROL_SENT_TO_PRINTER, SetJob, SetJob function [Windows GDI], SetJobA, SetJobW, _win32_SetJob, gdi.setjob, winspool/SetJob, winspool/SetJobA, winspool/SetJobW
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
req.unicode-ansi: SetJobW (Unicode) and SetJobA (ANSI)
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
-	WinSpool.drv
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	SetJob
-	SetJobA
-	SetJobW
product: Windows
targetos: Windows
req.lib: WinSpool.lib
req.dll: WinSpool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetJobW function


## -description


The <b>SetJob</b> function pauses, resumes, cancels, or restarts a print job on a specified printer. You can also use the <b>SetJob</b> function to set print job parameters, such as the print job priority and the document name.

You can use the <b>SetJob</b> function to give a command to a print job, or to set print job parameters, or to do both in the same call. The value of the <i>Command</i> parameter does not affect how the function uses the <i>Level</i> and <i>pJob</i> parameters. Also, you can use <b>SetJob</b> with <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> to link together a set of print jobs. See Remarks for more information.


## -parameters




### -param hPrinter [in]

A handle to the printer object of interest. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>, <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>, or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param JobId [in]

Identifier that specifies the print job. You obtain a print job identifier by calling the <a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a> function or the <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> function.

If the <i>Level</i> parameter is set to 3, the <i>JobId</i> parameter must match the <b>JobId</b> member of the <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> structure pointed to by <i>pJob</i>


### -param Level [in]

The type of job information structure pointed to by the <i>pJob</i> parameter.

<b>All versions of Windows</b>: You can set the <i>Level</i> parameter to 0, 1, or 2. When you set <i>Level</i> to 0, <i>pJob</i> should be <b>NULL</b>. Use these values when you are not setting any print job parameters.

You can also set the <i>Level</i> parameter to 3.

Starting with <b>Windows Vista</b>: You can also set the <i>Level</i> parameter to 4.


### -param pJob [in]

A pointer to a structure that sets the print job parameters.

<b>All versions of Windows</b>: <i>pJob</i> can point to a <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a> or <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a> structure.

<i>pJob</i> can also point to a <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> structure. You must have <b>JOB_ACCESS_ADMINISTER</b> access permission for the jobs specified by the <b>JobId</b> and <b>NextJobId</b> members of the <b>JOB_INFO_3</b> structure.

Starting with <b>Windows Vista</b>: <i>pJob</i> can also point to a <a href="https://msdn.microsoft.com/90932ae2-ea9e-43bc-9a1d-c68223f6d0ee">JOB_INFO_4</a> structure.

If the <i>Level</i> parameter is 0, <i>pJob</i> should be <b>NULL</b>.


### -param Command [in]

The print job operation to perform. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_CANCEL"></a><a id="job_control_cancel"></a><dl>
<dt><b>JOB_CONTROL_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
Do not use. To delete a print job, use <b>JOB_CONTROL_DELETE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_PAUSE"></a><a id="job_control_pause"></a><dl>
<dt><b>JOB_CONTROL_PAUSE</b></dt>
</dl>
</td>
<td width="60%">
Pause the print job.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_RESTART"></a><a id="job_control_restart"></a><dl>
<dt><b>JOB_CONTROL_RESTART</b></dt>
</dl>
</td>
<td width="60%">
Restart the print job. A job can only be restarted if it was printing.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_RESUME"></a><a id="job_control_resume"></a><dl>
<dt><b>JOB_CONTROL_RESUME</b></dt>
</dl>
</td>
<td width="60%">
Resume a paused print job.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_DELETE"></a><a id="job_control_delete"></a><dl>
<dt><b>JOB_CONTROL_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Delete the print job.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_SENT_TO_PRINTER"></a><a id="job_control_sent_to_printer"></a><dl>
<dt><b>JOB_CONTROL_SENT_TO_PRINTER</b></dt>
</dl>
</td>
<td width="60%">
Used by port monitors to end the print job.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_LAST_PAGE_EJECTED"></a><a id="job_control_last_page_ejected"></a><dl>
<dt><b>JOB_CONTROL_LAST_PAGE_EJECTED</b></dt>
</dl>
</td>
<td width="60%">
Used by language monitors to end the print job.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_RETAIN"></a><a id="job_control_retain"></a><dl>
<dt><b>JOB_CONTROL_RETAIN</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later</b>: Keep the job in the queue after it prints.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_CONTROL_RELEASE"></a><a id="job_control_release"></a><dl>
<dt><b>JOB_CONTROL_RELEASE</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later</b>:  Release the print job.

</td>
</tr>
</table>
 

You can use the same call to the <b>SetJob</b> function to set print job parameters and to give a command to a print job. Thus, <i>Command</i> does not need to be 0 if you are setting print job parameters, although it can be.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
You can use the <b>SetJob</b> function to set various print job parameters by supplying a pointer to a <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>, <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>, <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a>, or <a href="https://msdn.microsoft.com/90932ae2-ea9e-43bc-9a1d-c68223f6d0ee">JOB_INFO_4</a> structure that contains the necessary data.

To remove or delete all of the print jobs for a particular printer, call the <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> function with its <i>Command</i> parameter set to <b>PRINTER_CONTROL_PURGE</b>.

The following members of a <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>, <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>, or <a href="https://msdn.microsoft.com/90932ae2-ea9e-43bc-9a1d-c68223f6d0ee">JOB_INFO_4</a> structure are ignored on a call to <b>SetJob</b>: <b>JobId</b>, <b>pPrinterName</b>, <b>pMachineName</b>, <b>pUserName</b>, <b>pDrivername</b>, <b>Size</b>, <b>Submitted</b>, <b>Time</b>, and <b>TotalPages</b>.

You must have <b>PRINTER_ACCESS_ADMINISTER</b> access permission for a printer in order to change a print job's position in the print queue.

If you do not want to set a print job's position in the print queue, you should set the <b>Position</b> member of the <a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>, <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>, or <a href="https://msdn.microsoft.com/90932ae2-ea9e-43bc-9a1d-c68223f6d0ee">JOB_INFO_4</a> structure to <b>JOB_POSITION_UNSPECIFIED</b>.

Use the <b>SetJob</b> function with the <a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a> structure to link together a set of print jobs (also known as a chain). This is useful in situations where a single document consists of several parts that you want to render separately. To print jobs A, B, C, and D in order, call <b>SetJob</b> with <a href="https://msdn.microsoft.com/90932ae2-ea9e-43bc-9a1d-c68223f6d0ee">JOB_INFO_4</a> to link A to B, B to C, and C to D.

If you link print jobs, note the following:

<ul>
<li>Jobs can be added to the beginning or end of a chain.</li>
<li>All jobs in the chain must have the same data type.</li>
<li>
The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all. There are two ways to keep the chain from printing prematurely:

<ul>
<li>Pause the first job in the chain until the chain is completely linked. The paused state of the first job governs the state of all jobs in the chain.</li>
<li>Keep the first job incomplete, that is, do not call <a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a> or <a href="https://msdn.microsoft.com/a103a29c-be4d-491e-9b04-84571fe969a5">ScheduleJob</a> for the first job. However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</li>
</ul>
</li>
<li>The application must handle the case where the user deletes a job in the chain before the chain finishes printing. <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>INVALID_PARAMETER</b> when a JobID does not exist.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a>



<a href="https://msdn.microsoft.com/57e59f84-d2a0-4722-b0fc-6673f7bb5c57">GetJob</a>



<a href="https://msdn.microsoft.com/d42ada89-6bc7-4006-81d9-dbcc0347edd3">JOB_INFO_1</a>



<a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>



<a href="https://msdn.microsoft.com/a110f555-dc33-450c-ae77-ea26f0f69448">JOB_INFO_3</a>



<a href="https://msdn.microsoft.com/90932ae2-ea9e-43bc-9a1d-c68223f6d0ee">JOB_INFO_4</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

