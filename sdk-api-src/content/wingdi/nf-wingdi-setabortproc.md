---
UID: NF:wingdi.SetAbortProc
title: SetAbortProc function (wingdi.h)
description: The SetAbortProc function sets the application-defined abort function that allows a print job to be canceled during spooling.
helpviewer_keywords: ["SetAbortProc","SetAbortProc function [Windows GDI]","_win32_SetAbortProc","gdi.setabortproc","wingdi/SetAbortProc"]
old-location: gdi\setabortproc.htm
tech.root: xps
ms.assetid: 5b6333fc-f1c3-4c76-906c-0fd13bb73953
ms.date: 12/05/2018
ms.keywords: SetAbortProc, SetAbortProc function [Windows GDI], _win32_SetAbortProc, gdi.setabortproc, wingdi/SetAbortProc
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
 - SetAbortProc
 - wingdi/SetAbortProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetAbortProc
---

# SetAbortProc function


## -description

The <b>SetAbortProc</b> function sets the application-defined abort function that allows a print job to be canceled during spooling.

## -parameters

### -param hdc [in]

Handle to the device context for the print job.

### -param proc [in]

Pointer to the application-defined abort function. For more information about the callback function, see the <a href="/windows/desktop/api/wingdi/nc-wingdi-abortproc">AbortProc</a> callback function.

## -returns

If the function succeeds, the return value is greater than zero.

If the function fails, the return value is SP_ERROR.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>

#### Examples

For an example, see <a href="/windows/desktop/printdocs/preparing-to-print">How to Collect Print Job  Information from the User</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-abortdoc">AbortDoc</a>



<a href="/windows/desktop/api/wingdi/nc-wingdi-abortproc">AbortProc</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>