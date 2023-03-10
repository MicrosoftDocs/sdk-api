---
UID: NF:commctrl.RemoveWindowSubclass
title: RemoveWindowSubclass function (commctrl.h)
description: Removes a subclass callback from a window.
helpviewer_keywords: ["RemoveWindowSubclass","RemoveWindowSubclass function [Windows Shell]","commctrl/RemoveWindowSubclass","inet_RemoveWindowSubclass","shell.RemoveWindowSubclass"]
old-location: shell\RemoveWindowSubclass.htm
tech.root: shell
ms.assetid: 09f27240-f3af-4791-afcb-a82bda79712a
ms.date: 12/05/2018
ms.keywords: RemoveWindowSubclass, RemoveWindowSubclass function [Windows Shell], commctrl/RemoveWindowSubclass, inet_RemoveWindowSubclass, shell.RemoveWindowSubclass
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
 - RemoveWindowSubclass
 - commctrl/RemoveWindowSubclass
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
 - RemoveWindowSubclass
req.apiset: ext-ms-win-shell-comctl32-window-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# RemoveWindowSubclass function


## -description

Removes a subclass callback from a window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

The handle of the window being subclassed.

### -param pfnSubclass [in]

Type: <b><a href="/windows/desktop/api/commctrl/nc-commctrl-subclassproc">SUBCLASSPROC</a></b>

A pointer to a window procedure. This pointer and the subclass ID uniquely identify this subclass callback. For the callback function prototype, see <a href="/windows/desktop/api/commctrl/nc-commctrl-subclassproc">SUBCLASSPROC</a>.

### -param uIdSubclass [in]

Type: <b>UINT_PTR</b>

The <b>UINT_PTR</b> subclass ID. This ID and the callback pointer uniquely identify this subclass callback. Note: On 64-bit versions of Windows this is a 64-bit value.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the subclass callback was successfully removed; otherwise, <b>FALSE</b>.

## -remarks

Subclass callbacks are identified by their combination of the callback address and the subclass ID defined by the calling process.

The SUBCLASS module defines helper functions that are used to subclass windows. The code maintains a single property on the subclassed window and dispatches various subclass callbacks to its clients as required. The client is provided reference data and a default processing API.

No reference counting is performed for the callback; it may repeatedly call <a href="/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass">SetWindowSubclass</a> to alter the value of its reference data element.

<div class="alert"><b>Warning</b>  You cannot use the subclassing helper functions to subclass a window across threads.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc">DefSubclassProc</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass">GetWindowSubclass</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass">SetWindowSubclass</a>
