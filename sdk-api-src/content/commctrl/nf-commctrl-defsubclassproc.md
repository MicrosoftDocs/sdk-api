---
UID: NF:commctrl.DefSubclassProc
title: DefSubclassProc function (commctrl.h)
description: Calls the next handler in a window's subclass chain. The last handler in the subclass chain calls the original window procedure for the window.
helpviewer_keywords: ["DefSubclassProc","DefSubclassProc function [Windows Shell]","commctrl/DefSubclassProc","inet_DefSubclassProc","shell.DefSubclassProc"]
old-location: shell\DefSubclassProc.htm
tech.root: shell
ms.assetid: 43b1efa5-11da-4a95-8d81-b0d8ae64733a
ms.date: 12/05/2018
ms.keywords: DefSubclassProc, DefSubclassProc function [Windows Shell], commctrl/DefSubclassProc, inet_DefSubclassProc, shell.DefSubclassProc
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 5.8 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DefSubclassProc
 - commctrl/DefSubclassProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DefSubclassProc
req.apiset: ext-ms-win-shell-comctl32-window-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DefSubclassProc function


## -description

Calls the next handler in a window's subclass chain. The last handler in the subclass chain calls the original window procedure for the window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window being subclassed.

### -param uMsg [in]

Type: <b>UINT</b>

A value of type unsigned <b>int</b> that specifies a window message.

### -param wParam [in]

Type: <b>WPARAM</b>

Specifies additional message information. The contents of this parameter depend on the value of the window message.

### -param lParam [in]

Type: <b>LPARAM</b>

Specifies additional message information. The contents of this parameter depend on the value of the window message. Note: On 64-bit versions of Windows LPARAM is a 64-bit value.

## -returns

Type: <b>LRESULT</b>

The returned value is specific to the message sent. This value should be ignored.

## -remarks

You do not need to call the default window procedure; this function calls it automatically.

The SUBCLASS module defines helper functions that are used to subclass windows. The code maintains a single property on the subclassed window and dispatches various subclass callbacks to its clients as required. The client is provided reference data and a default processing API.

A subclass callback is identified by a unique pairing of a callback function pointer and an unsigned ID value. Each callback can also store a single <b>DWORD</b> of reference data, which is passed to the callback function when it is called to filter messages. No reference counting is performed for the callback; it may repeatedly call <a href="/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass">SetWindowSubclass</a> to alter the value of its reference data element.

<div class="alert"><b>Warning</b>  You cannot use the subclassing helper functions to subclass a window across threads.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass">GetWindowSubclass</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass">RemoveWindowSubclass</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass">SetWindowSubclass</a>
