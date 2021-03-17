---
UID: NF:wingdi.EndPage
title: EndPage function (wingdi.h)
description: The EndPage function notifies the device that the application has finished writing to a page. This function is typically used to direct the device driver to advance to a new page.
helpviewer_keywords: ["EndPage","EndPage function [Windows GDI]","_win32_EndPage","gdi.endpage","wingdi/EndPage"]
old-location: gdi\endpage.htm
tech.root: xps
ms.assetid: 33e6d005-f00d-4b87-bf7c-fc79c1d05514
ms.date: 12/05/2018
ms.keywords: EndPage, EndPage function [Windows GDI], _win32_EndPage, gdi.endpage, wingdi/EndPage
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EndPage
 - wingdi/EndPage
dev_langs:
 - c++
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
 - EndPage
---

# EndPage function


## -description

The <b>EndPage</b> function notifies the device that the application has finished writing to a page. This function is typically used to direct the device driver to advance to a new page.

## -parameters

### -param hdc [in]

A handle to the device context for the print job.

## -returns

If the function succeeds, the return value is greater than zero.

If the function fails, the return value is less than or equal to zero.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a> function to change the device mode, if necessary, after calling the <b>EndPage</b> function. Note that a call to <b>ResetDC</b> resets all device context attributes back to default values. Neither <b>EndPage</b> nor <a href="/windows/desktop/api/wingdi/nf-wingdi-startpage">StartPage</a> resets the device context attributes. Device context attributes remain constant across subsequent pages. You do not need to re-select objects and set up the mapping mode again before printing the next page; however, doing so will produce the same results and reduce code differences between versions of Windows.

When a page in a spooled file exceeds approximately 350 MB, it may fail to print and not send an error message. For example, this can occur when printing large EMF files. The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.


#### Examples

For a sample program that uses this function, see <a href="/windows/desktop/printdocs/how-to--print-using-the-gdi-print-api">How To: Print Using the GDI Print API</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-startpage">StartPage</a>