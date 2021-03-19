---
UID: NC:wingdi.ABORTPROC
title: ABORTPROC (wingdi.h)
description: The AbortProc function is an application-defined callback function used with the SetAbortProc function.
helpviewer_keywords: ["AbortProc","AbortProc callback","AbortProc callback function [Windows GDI]","_win32_AbortProc","gdi.abortproc","wingdi/AbortProc"]
old-location: gdi\abortproc.htm
tech.root: xps
ms.assetid: 3728a491-28ff-49ec-9131-ed6238b2be3d
ms.date: 12/05/2018
ms.keywords: AbortProc, AbortProc callback, AbortProc callback function [Windows GDI], _win32_AbortProc, gdi.abortproc, wingdi/AbortProc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ABORTPROC
 - wingdi/ABORTPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - AbortProc
---

# ABORTPROC callback function


## -description

The <b>AbortProc</b> function is an application-defined callback function used with the <a href="/windows/desktop/api/wingdi/nf-wingdi-setabortproc">SetAbortProc</a> function. It is called when a print job is to be canceled during spooling. The <b>ABORTPROC</b> type defines a pointer to this callback function. <b>AbortProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

### -param unnamedParam2

#### - hdc [in]

A handle to the device context for the print job.


#### - iError [in]

Specifies whether an error has occurred. This parameter is zero if no error has occurred; it is SP_OUTOFDISK if Print Manager is currently out of disk space and more disk space will become available if the application waits.

## -returns

The callback function should return <b>TRUE</b> to continue the print job or <b>FALSE</b> to cancel the print job.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
If the <i>iError</i> parameter is SP_OUTOFDISK, the application need not cancel the print job. If it does not cancel the job, it must yield to Print Manager by calling the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setabortproc">SetAbortProc</a>