---
UID: NF:winspool.EndPagePrinter
title: EndPagePrinter function
author: windows-driver-content
description: The EndPagePrinter function notifies the print spooler that the application is at the end of a page in a print job.
old-location: gdi\endpageprinter.htm
old-project: printdocs
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EndPagePrinter, EndPagePrinter function [Windows GDI], _win32_EndPagePrinter, gdi.endpageprinter, winspool/EndPagePrinter
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
-	EndPagePrinter
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EndPagePrinter function


## -description


The <b>EndPagePrinter</b> function notifies the print spooler that the application is at the end of a page in a print job.


## -parameters




### -param hPrinter [in]

Handle to the printer for which the page will be concluded. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The sequence for a print job is as follows:

<ol>
<li>To begin a print job, call <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>.</li>
<li>To begin each page, call <a href="https://msdn.microsoft.com/8ac7c47b-b3a7-4642-bfb7-54e014139fbf">StartPagePrinter</a>.</li>
<li>To write data to a page, call <a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>.</li>
<li>To end each page, call <b>EndPagePrinter</b>.</li>
<li>Repeat 2, 3, and 4 for as many pages as necessary.</li>
<li>To end the print job, call <a href="https://msdn.microsoft.com/13c713e8-cc24-4191-8b1e-967b9e20e541">EndDocPrinter</a>.</li>
</ol>

         When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message. For example, this can occur when printing large EMF files. The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.




## -see-also




<a href="https://msdn.microsoft.com/13c713e8-cc24-4191-8b1e-967b9e20e541">EndDocPrinter</a>



<a href="https://msdn.microsoft.com/aceb88b9-375b-4cd2-996a-c369f590154e">EndPagePrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>



<a href="https://msdn.microsoft.com/8ac7c47b-b3a7-4642-bfb7-54e014139fbf">StartPagePrinter</a>



<a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>
 

 

