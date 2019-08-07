---
UID: NF:wingdi.StartDocW
title: StartDocW function (wingdi.h)
author: windows-sdk-content
description: The StartDoc function starts a print job.
old-location: gdi\startdoc.htm
tech.root: printdocs
ms.assetid: 53143463-b9fc-4378-aea9-da6c73a7cd03
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StartDoc, StartDoc function [Windows GDI], StartDocA, StartDocW, _win32_StartDoc, gdi.startdoc, wingdi/StartDoc, wingdi/StartDocA, wingdi/StartDocW
ms.topic: function
f1_keywords:
- wingdi/StartDoc
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StartDocW (Unicode) and StartDocA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- gdi32.dll
- Ext-MS-Win-GDI-print-l1-1-0.dll
- GDI32Full.dll
api_name:
- StartDoc
- StartDocA
- StartDocW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StartDocW function


## -description


The <b>StartDoc</b> function starts a print job.


## -parameters




### -param hdc [in]

A handle to the device context for the print job.


### -param lpdi [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-docinfoa">DOCINFO</a> structure containing the name of the document file and the name of the output file.


## -returns



If the function succeeds, the return value is greater than zero. This value is the print job identifier for the document.

If the function fails, the return value is less than or equal to zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Applications should call the <b>StartDoc</b> function immediately before beginning a print job. Using this function ensures that multipage documents are not interspersed with other print jobs.

Applications can use the value returned by <b>StartDoc</b> to retrieve or set the priority of a print job. Call the <a href="https://docs.microsoft.com/windows/desktop/printdocs/getjob">GetJob</a> or <a href="https://docs.microsoft.com/windows/desktop/printdocs/setjob">SetJob</a> function and supply this value as one of the required arguments.


#### Examples

For a sample program that uses this function, see <a href="https://docs.microsoft.com/windows/desktop/printdocs/how-to--print-using-the-gdi-print-api">How To: Print Using the GDI Print API</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-docinfoa">DOCINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/getjob">GetJob</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/setjob">SetJob</a>
 

 

