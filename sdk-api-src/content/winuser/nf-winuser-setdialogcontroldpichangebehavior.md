---
UID: NF:winuser.SetDialogControlDpiChangeBehavior
title: SetDialogControlDpiChangeBehavior function (winuser.h)
description: Overrides the default per-monitor DPI scaling behavior of a child window in a dialog.
helpviewer_keywords: ["SetDialogControlDpiChangeBehavior","SetDialogResizeBehavior","SetDialogResizeBehavior function [High DPI]","hidpi.setdialogresizebehavior","winuser/SetDialogResizeBehavior"]
old-location: hidpi\setdialogresizebehavior.htm
tech.root: hidpi
ms.assetid: 52BB557B-0D70-4189-9BD0-EB94188EA4E7
ms.date: 12/05/2018
ms.keywords: SetDialogControlDpiChangeBehavior, SetDialogResizeBehavior, SetDialogResizeBehavior function [High DPI], hidpi.setdialogresizebehavior, winuser/SetDialogResizeBehavior
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
 - SetDialogControlDpiChangeBehavior
 - winuser/SetDialogControlDpiChangeBehavior
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
 - SetDialogResizeBehavior
---

# SetDialogControlDpiChangeBehavior function


## -description

Overrides the default per-monitor DPI scaling behavior of a child window in a dialog.

## -parameters

### -param hWnd

A handle for the window whose behavior will be modified.

### -param mask

A mask specifying the subset of flags to be changed.

### -param values

The desired value to be set for the specified subset of flags.

## -returns

This function returns TRUE if the operation was successful, and FALSE otherwise. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Possible errors are <b>ERROR_INVALID_HANDLE</b> if passed an invalid HWND, and <b>ERROR_ACCESS_DENIED</b> if the windows belongs to another process.

## -remarks

The behaviors are specified as values from the <a href="/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a> enum. This function follows the typical two-parameter approach to setting flags, where a mask specifies the subset of the flags to be changed.

It is valid to set these behaviors on <i>any</i> window. It does not matter if the window is currently a child of a dialog at the point in time that SetDialogControlDpiChangeBehavior is called. The behaviors are retained and will take effect only when the window is an immediate child of a dialog that has per-monitor DPI scaling enabled.

This API influences individual controls within dialogs. The dialog-wide per-monitor DPI scaling behavior is controlled by <a href="/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior">SetDialogDpiChangeBehavior</a>.

## -see-also

<a href="/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior">GetDialogControlDpiChangeBehavior</a>