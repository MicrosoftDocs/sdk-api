---
UID: NF:winspool.StartDocPrinterW
title: StartDocPrinterW function
author: windows-driver-content
description: The StartDocPrinter function notifies the print spooler that a document is to be spooled for printing.
old-location: gdi\startdocprinter.htm
old-project: printdocs
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: StartDocPrinter, StartDocPrinter function [Windows GDI], StartDocPrinterA, StartDocPrinterW, _win32_StartDocPrinter, gdi.startdocprinter, winspool/StartDocPrinter, winspool/StartDocPrinterA, winspool/StartDocPrinterW
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
req.unicode-ansi: StartDocPrinterW (Unicode) and StartDocPrinterA (ANSI)
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
-	StartDocPrinter
-	StartDocPrinterA
-	StartDocPrinterW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# StartDocPrinterW function


## -description


The <b>StartDocPrinter</b> function notifies the print spooler that a document is to be spooled for printing.


## -parameters




### -param hPrinter [in]

A handle to the printer. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param Level [in]

The version of the structure to which <i>pDocInfo</i> points. This value must be 1.


### -param pDocInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/142d988b-dd74-4312-8b27-331a7ec70344">DOC_INFO_1</a> structure that describes the document to print.


## -returns



If the function succeeds, the return value identifies the print job.

If the function fails, the return value is zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The typical sequence for a print job is as follows:

<ol>
<li>To begin a print job, call <b>StartDocPrinter</b>.</li>
<li>To begin each page, call <a href="https://msdn.microsoft.com/8ac7c47b-b3a7-4642-bfb7-54e014139fbf">StartPagePrinter</a>.</li>
<li>To write data to a page, call <a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>.</li>
<li>To end each page, call <a href="https://msdn.microsoft.com/aceb88b9-375b-4cd2-996a-c369f590154e">EndPagePrinter</a>.</li>
<li>Repeat 2, 3, and 4 for as many pages as necessary.</li>
<li>To end the print job, call <a href="https://msdn.microsoft.com/13c713e8-cc24-4191-8b1e-967b9e20e541">EndDocPrinter</a>.</li>
</ol>
Note that calling <a href="https://msdn.microsoft.com/8ac7c47b-b3a7-4642-bfb7-54e014139fbf">StartPagePrinter</a> and <a href="https://msdn.microsoft.com/aceb88b9-375b-4cd2-996a-c369f590154e">EndPagePrinter</a> may not be necessary, such as if the print data type includes the page information.

When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message. For example, this can occur when printing large EMF files. The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.


#### Examples

For a sample program that uses this function, see <a href="https://msdn.microsoft.com/C212DD92-2B90-45BC-8746-29C193FBDF69">How To: Print Using the GDI Print API</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a>



<a href="https://msdn.microsoft.com/142d988b-dd74-4312-8b27-331a7ec70344">DOC_INFO_1</a>



<a href="https://msdn.microsoft.com/d62333f3-cc39-4c9b-8fb3-02a2d24bbbad">DOC_INFO_2</a>



<a href="https://msdn.microsoft.com/13c713e8-cc24-4191-8b1e-967b9e20e541">EndDocPrinter</a>



<a href="https://msdn.microsoft.com/aceb88b9-375b-4cd2-996a-c369f590154e">EndPagePrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>



<a href="https://msdn.microsoft.com/8ac7c47b-b3a7-4642-bfb7-54e014139fbf">StartPagePrinter</a>



<a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>
 

 

