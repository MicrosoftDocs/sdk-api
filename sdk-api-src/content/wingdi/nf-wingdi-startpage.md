---
UID: NF:wingdi.StartPage
title: StartPage function (wingdi.h)
description: The StartPage function prepares the printer driver to accept data.
helpviewer_keywords: ["StartPage","StartPage function [Windows GDI]","_win32_StartPage","gdi.startpage","wingdi/StartPage"]
old-location: gdi\startpage.htm
tech.root: xps
ms.assetid: b2bc0593-5eaf-40af-aa38-fbdfa1ea5f76
ms.date: 12/05/2018
ms.keywords: StartPage, StartPage function [Windows GDI], _win32_StartPage, gdi.startpage, wingdi/StartPage
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
 - StartPage
 - wingdi/StartPage
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
 - StartPage
---

# StartPage function


## -description

The <b>StartPage</b> function prepares the printer driver to accept data.

## -parameters

### -param hdc [in]

A handle to the device context for the print job.

## -returns

If the function succeeds, the return value is greater than zero.

If the function fails, the return value is less than or equal to zero.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The system disables the <a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a> function between calls to the <b>StartPage</b> and <a href="/windows/desktop/api/wingdi/nf-wingdi-endpage">EndPage</a> functions. This means that you cannot change the device mode except at page boundaries. After calling <b>EndPage</b>, you can call <b>ResetDC</b> to change the device mode, if necessary. Note that a call to <b>ResetDC</b> resets all device context attributes back to default values.

Neither <a href="/windows/desktop/api/wingdi/nf-wingdi-endpage">EndPage</a> nor <b>StartPage</b> resets the device context attributes. Device context attributes remain constant across subsequent pages. You do not need to re-select objects and set up the mapping mode again before printing the next page; however, doing so will produce the same results and reduce code differences between versions of Windows.


#### Examples

For a sample program that uses this function, see <a href="/windows/desktop/printdocs/how-to--print-using-the-gdi-print-api">How To: Print Using the GDI Print API</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-endpage">EndPage</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a>