---
UID: NF:winspool.AddJobW
title: AddJobW function
author: windows-driver-content
description: The AddJob function adds a print job to the list of print jobs that can be scheduled by the print spooler. The function retrieves the name of the file you can use to store the job.
old-location: gdi\addjob.htm
old-project: printdocs
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddJob, AddJob function [Windows GDI], AddJobA, AddJobW, _win32_AddJob, gdi.addjob, winspool/AddJob, winspool/AddJobA, winspool/AddJobW
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
req.unicode-ansi: AddJobW (Unicode) and AddJobA (ANSI)
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
-	AddJob
-	AddJobA
-	AddJobW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddJobW function


## -description


The <b>AddJob</b> function adds a print job to the list of print jobs that can be scheduled by the print spooler. The function retrieves the name of the file you can use to store the job.
<div class="alert"><b>Note</b>  In Windows 8 and later operating systems, we do not recommended using <b>AddJob</b> directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where <b>AddJob</b> will fail.  Instead you are advised to use <a href="https://msdn.microsoft.com/3115c9e0-05c9-462d-8238-fc035ea32d4e">GDI Print API</a>, <a href="https://msdn.microsoft.com/df06ddcb-e573-461c-99a3-8f108fe2c143">XPS Print API</a>, <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>, or the appropriate method from the <a href="https://msdn.microsoft.com/a77f4765-4366-4e45-bfaa-e50c0e711bf8">Windows.Graphics.Printing</a> namespace,  depending on the print scenario.<p class="note">If you try to print to a queue using <b>File:</b> or <b>PORTPROMPT:</b>, <b>AddJob</b> will Return the  NOT_SUPPORTED error.

</div><div> </div>

## -parameters




### -param hPrinter [in]

A handle that specifies the printer for the print job. This must be a local printer that is configured as a spooled printer. If <i>hPrinter</i> is a handle to a remote printer connection, or if the printer is configured for direct printing, the <b>AddJob</b> function fails. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param Level [in]

The version of the print job information data structure that the function stores into the buffer pointed to by <i>pData</i>. Set this parameter to one.


### -param pData [out]

A pointer to a buffer that receives an <a href="https://msdn.microsoft.com/de915932-11a7-47e8-9be9-edab76d94189">ADDJOB_INFO_1</a> data structure and a path string.


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>. The buffer needs to be large enough to contain an <a href="https://msdn.microsoft.com/de915932-11a7-47e8-9be9-edab76d94189">ADDJOB_INFO_1</a> structure and a path string.


### -param pcbNeeded [out]

A pointer to a variable that receives the total size, in bytes, of the <a href="https://msdn.microsoft.com/de915932-11a7-47e8-9be9-edab76d94189">ADDJOB_INFO_1</a> data structure plus the path string. If this value is less than or equal to <i>cbBuf</i> and the function succeeds, this is the actual number of bytes written to the buffer pointed to by <i>pData</i>. If this number is greater than <i>cbBuf</i>, the buffer is too small, and you must call the function again with a buffer size at least as large as *<i>pcbNeeded</i>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
You can call the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function to open the spool file specified by the <b>Path</b> member of the <a href="https://msdn.microsoft.com/de915932-11a7-47e8-9be9-edab76d94189">ADDJOB_INFO_1</a> structure, and then call the <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function to write print job data to it. After that is done, call the <a href="https://msdn.microsoft.com/a103a29c-be4d-491e-9b04-84571fe969a5">ScheduleJob</a> function to notify the print spooler that the print job can now be scheduled by the spooler for printing.




## -see-also




<a href="https://msdn.microsoft.com/de915932-11a7-47e8-9be9-edab76d94189">ADDJOB_INFO_1</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/3115c9e0-05c9-462d-8238-fc035ea32d4e">GDI Print API</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/a103a29c-be4d-491e-9b04-84571fe969a5">ScheduleJob</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>



<a href="https://msdn.microsoft.com/a77f4765-4366-4e45-bfaa-e50c0e711bf8">Windows.Graphics.Printing</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>



<a href="https://msdn.microsoft.com/df06ddcb-e573-461c-99a3-8f108fe2c143">XPS Print API</a>
 

 

