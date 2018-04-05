---
UID: NF:winspool.ReportJobProcessingProgress
title: ReportJobProcessingProgress function
author: windows-driver-content
description: Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.
old-location: gdi\reportjobprocessingprogress.htm
old-project: printdocs
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ReportJobProcessingProgress, ReportJobProcessingProgress function [Windows GDI], _win32_ReportJobProcessingProgress, gdi.reportjobprocessingprogress, winspool/ReportJobProcessingProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	WinSpool.Drv
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	ReportJobProcessingProgress
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ReportJobProcessingProgress function


## -description


Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.


## -parameters




### -param printerHandle [in]

A printer handle for which the function is to retrieve information. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param jobId [in]

Identifies the print job for which to retrieve data. Use the <a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a> function or <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> function to get a print job identifier.


### -param jobOperation

Specifies whether the job is in the spooling phase or the rendering phase.


### -param jobProgress

Specifies what part of the processing is currently underway. This value refers to events in either the spooling or rendering phase depending on the value of <i>jobOperation</i>.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> will contain an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>ReportJobProcessingProgress</b> will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.  <b>ReportJobProcessingProgress</b> will fail if it is called when the XPS print job is not in the spooling or rendering phase.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/14871d29-59e4-45a2-9697-12550c58396c">EPrintXPSJobOperation</a>



<a href="https://msdn.microsoft.com/4fa5b749-e4f9-4f08-97b5-e58f82d0b485">EPrintXPSJobProgress</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

