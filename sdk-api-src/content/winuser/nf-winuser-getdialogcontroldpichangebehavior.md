---
UID: NF:winuser.GetDialogControlDpiChangeBehavior
title: GetDialogControlDpiChangeBehavior function (winuser.h)
description: Retrieves and per-monitor DPI scaling behavior overrides of a child window in a dialog.
helpviewer_keywords: ["GetDialogControlDpiChangeBehavior","GetDialogControlDpiChangeBehavior function [High DPI]","hidpi.getdialogresizebehavior","winuser/GetDialogControlDpiChangeBehavior"]
old-location: hidpi\getdialogresizebehavior.htm
tech.root: hidpi
ms.assetid: 1651353F-5823-41B8-AE52-016AEBA6C4F0
ms.date: 12/05/2018
ms.keywords: GetDialogControlDpiChangeBehavior, GetDialogControlDpiChangeBehavior function [High DPI], hidpi.getdialogresizebehavior, winuser/GetDialogControlDpiChangeBehavior
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDialogControlDpiChangeBehavior
 - winuser/GetDialogControlDpiChangeBehavior
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetDialogControlDpiChangeBehavior
---

# GetDialogControlDpiChangeBehavior function


## -description

Retrieves and per-monitor DPI scaling behavior overrides of a child window in a dialog.

## -parameters

### -param hWnd

The handle for the window to examine.

## -returns

The flags set on the given window. If passed an invalid handle, this function will return zero, and set its <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">last error</a> to <b>ERROR_INVALID_HANDLE</b>.

## -see-also

<a href="/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior">SetDialogControlDpiChangeBehavior</a>