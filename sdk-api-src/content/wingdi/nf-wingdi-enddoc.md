---
UID: NF:wingdi.EndDoc
title: EndDoc function (wingdi.h)
description: The EndDoc function ends a print job.
helpviewer_keywords: ["EndDoc","EndDoc function [Windows GDI]","_win32_EndDoc","gdi.enddoc","wingdi/EndDoc"]
old-location: gdi\enddoc.htm
tech.root: xps
ms.assetid: bf63ea0f-cc73-4943-9c84-52b3b77e141c
ms.date: 12/05/2018
ms.keywords: EndDoc, EndDoc function [Windows GDI], _win32_EndDoc, gdi.enddoc, wingdi/EndDoc
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
 - EndDoc
 - wingdi/EndDoc
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
 - EndDoc
---

# EndDoc function


## -description

The <b>EndDoc</b> function ends a print job.

## -parameters

### -param hdc [in]

Handle to the device context for the print job.

## -returns

If the function succeeds, the return value is greater than zero.

If the function fails, the return value is less than or equal to zero.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Applications should call <b>EndDoc</b> immediately after finishing a print job.


#### Examples

For a sample program that uses this function, see <a href="/windows/desktop/printdocs/how-to--print-using-the-gdi-print-api">How To: Print Using the GDI Print API</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a>