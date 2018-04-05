---
UID: NF:winspool.ScheduleJob
title: ScheduleJob function
author: windows-driver-content
description: The ScheduleJob function requests that the print spooler schedule a specified print job for printing.
old-location: gdi\schedulejob.htm
old-project: printdocs
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ScheduleJob, ScheduleJob function [Windows GDI], _win32_ScheduleJob, gdi.schedulejob, winspool/ScheduleJob
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
-	ScheduleJob
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ScheduleJob function


## -description


The <b>ScheduleJob</b> function requests that the print spooler schedule a specified print job for printing.


## -parameters




### -param hPrinter [in]

A handle to the printer for the print job. This must be a local printer that is configured as a spooled printer. If <i>hPrinter</i> is a handle to a remote printer connection, or if the printer is configured for direct printing, the <b>ScheduleJob</b> function fails. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.

<i>hPrinter</i> must be the same printer handle specified in the call to <a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a> that obtained the <i>dwJobID</i> print job identifier.


### -param JobId

TBD




#### - dwJobID [in]

The print job to be scheduled. You obtain this print job identifier by calling the <a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a> function.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
You must successfully call the <a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a> function before calling the <b>ScheduleJob</b> function. <b>AddJob</b> obtains the print job identifier that you pass to <b>ScheduleJob</b> as <i>dwJobID</i>. Both calls must use the same value for <i>hPrinter</i>.

The <b>ScheduleJob</b> function checks for a valid spool file. If there is an invalid spool file, or if it is empty, <b>ScheduleJob</b> deletes both the spool file and the corresponding print job entry in the print spooler.




## -see-also




<a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

