---
UID: NF:commctrl.SetWindowSubclass
title: SetWindowSubclass function (commctrl.h)
description: Installs or updates a window subclass callback.
helpviewer_keywords: ["SetWindowSubclass","SetWindowSubclass function [Windows Shell]","commctrl/SetWindowSubclass","inet_SetWindowSubclass","shell.SetWindowSubclass"]
old-location: shell\SetWindowSubclass.htm
tech.root: shell
ms.assetid: 0b11144d-eb4e-462c-96d3-38c4bac48f2a
ms.date: 12/05/2018
ms.keywords: SetWindowSubclass, SetWindowSubclass function [Windows Shell], commctrl/SetWindowSubclass, inet_SetWindowSubclass, shell.SetWindowSubclass
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
 - SetWindowSubclass
 - commctrl/SetWindowSubclass
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
 - SetWindowSubclass
req.apiset: ext-ms-win-shell-comctl32-window-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# SetWindowSubclass function


## -description

Installs or updates a window subclass callback.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

The handle of the window being subclassed.

### -param pfnSubclass [in]

Type: <b><a href="/windows/desktop/api/commctrl/nc-commctrl-subclassproc">SUBCLASSPROC</a></b>

A pointer to a window procedure. This pointer and the subclass ID uniquely identify this subclass callback. For the callback function prototype, see <a href="/windows/desktop/api/commctrl/nc-commctrl-subclassproc">SUBCLASSPROC</a>.

### -param uIdSubclass [in]

Type: <b>UINT_PTR</b>

The subclass ID. This ID together with the subclass procedure uniquely identify a subclass. To remove a subclass, pass the subclass procedure and this value to the <a href="/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass">RemoveWindowSubclass</a> function. This value is passed to the subclass procedure in the uIdSubclass parameter.

### -param dwRefData [in]

Type: <b>DWORD_PTR</b>

<b>DWORD_PTR</b> to reference data. The meaning of this value is determined by the calling application. This value is passed to the subclass procedure in the dwRefData parameter. A different dwRefData is associated with each combination of window handle, subclass procedure and uIdSubclass.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the subclass callback was successfully installed; otherwise, <b>FALSE</b>.

## -remarks

Subclass callbacks are identified by the combination of the callback address and the caller-defined subclass ID. If the callback address and ID pair have not yet been installed, then this function installs the subclass. If the pair has already been installed, then this function just updates the reference data.

Each callback can store a single <b>DWORD_PTR</b> of reference data, which is passed to the callback function when it is called to filter messages. No reference counting is performed for the callback; it may repeatedly call <b>SetWindowSubclass</b> to alter the value of its reference data element.

<div class="alert"><b>Warning</b>  You cannot use the subclassing helper functions to subclass a window across threads.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc">DefSubclassProc</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass">GetWindowSubclass</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass">RemoveWindowSubclass</a>
