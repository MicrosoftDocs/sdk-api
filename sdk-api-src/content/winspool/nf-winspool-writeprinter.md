---
UID: NF:winspool.WritePrinter
title: WritePrinter function
author: windows-driver-content
description: The WritePrinter function notifies the print spooler that data should be written to the specified printer.
old-location: gdi\writeprinter.htm
old-project: printdocs
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WritePrinter, WritePrinter function [Windows GDI], _win32_WritePrinter, gdi.writeprinter, winspool/WritePrinter
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
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	WinSpool.Drv
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	WritePrinter
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WritePrinter function


## -description


The <b>WritePrinter</b> function notifies the print spooler that data should be written to the specified printer.
<div class="alert"><b>Note</b>  <b>WritePrinter</b> only supports GDI printing and must not be used for XPS printing.  If your print job uses the XPS or the OpenXPS print path, then use the <a href="http://msdn.microsoft.com/en-us/library/windows/desktop/ff686814(v=vs.85).aspx">XPS Print API</a>. Sending XPS or OpenXPS print jobs to the spooler using <b>WritePrinter</b> is not supported and can result in undetermined results.</div><div> </div>

## -parameters




### -param hPrinter [in]

A handle to the printer. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pBuf [in]

A pointer to an array of bytes that contains the data that should be written to the printer.


### -param cbBuf [in]

The size, in bytes, of the array.


### -param pcWritten [out]

A pointer to a value that receives the number of bytes of data that were written to the printer.


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
<li>To write data to a page, call <b>WritePrinter</b>.</li>
<li>To end each page, call <a href="https://msdn.microsoft.com/aceb88b9-375b-4cd2-996a-c369f590154e">EndPagePrinter</a>.</li>
<li>Repeat 2, 3, and 4 for as many pages as necessary.</li>
<li>To end the print job, call <a href="https://msdn.microsoft.com/13c713e8-cc24-4191-8b1e-967b9e20e541">EndDocPrinter</a>.</li>
</ol>
When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings. Documents output when the value of the <i>pDatatype</i> member of the <a href="https://msdn.microsoft.com/142d988b-dd74-4312-8b27-331a7ec70344">DOC_INFO_1</a> structure that was passed in the  <i>pDocInfo</i> parameter of the <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a> call is "RAW" must fully describe the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>-style print job settings in the language understood by the hardware.


         In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message. For example, this can occur when printing large EMF files. The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap. In Windows XP and later versions of Windows, EMF files must be 2GB or less in size. If <b>WritePrinter</b> is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.


#### Examples

For a sample program that uses this function, see <a href="https://msdn.microsoft.com/C212DD92-2B90-45BC-8746-29C193FBDF69">How To: Print Using the GDI Print API</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/13c713e8-cc24-4191-8b1e-967b9e20e541">EndDocPrinter</a>



<a href="https://msdn.microsoft.com/aceb88b9-375b-4cd2-996a-c369f590154e">EndPagePrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>



<a href="https://msdn.microsoft.com/8ac7c47b-b3a7-4642-bfb7-54e014139fbf">StartPagePrinter</a>



<a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>
 

 

