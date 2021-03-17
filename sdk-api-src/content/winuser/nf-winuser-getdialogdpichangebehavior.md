---
UID: NF:winuser.GetDialogDpiChangeBehavior
title: GetDialogDpiChangeBehavior function (winuser.h)
description: Returns the flags that might have been set on a given dialog by an earlier call to SetDialogDpiChangeBehavior.
helpviewer_keywords: ["GetDialogDpiChangeBehavior","GetDialogDpiChangeBehavior function [High DPI]","hidpi.getdialogdpichangebehavior","winuser/GetDialogDpiChangeBehavior"]
old-location: hidpi\getdialogdpichangebehavior.htm
tech.root: hidpi
ms.assetid: 8ED61C77-36C8-453B-BAB1-505CE4974D63
ms.date: 12/05/2018
ms.keywords: GetDialogDpiChangeBehavior, GetDialogDpiChangeBehavior function [High DPI], hidpi.getdialogdpichangebehavior, winuser/GetDialogDpiChangeBehavior
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
 - GetDialogDpiChangeBehavior
 - winuser/GetDialogDpiChangeBehavior
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
 - GetDialogDpiChangeBehavior
---

# GetDialogDpiChangeBehavior function


## -description

Returns the flags that might have been set on a given dialog by an earlier call to <a href="/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior">SetDialogDpiChangeBehavior</a>.

 If that function was never called on the dialog, the return value will be zero.

## -parameters

### -param hDlg

The handle for the dialog to examine.

## -returns

The flags set on the given dialog. If passed an invalid handle, this function will return zero, and set its <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">last error</a> to <b>ERROR_INVALID_HANDLE</b>.

## -remarks

It can be difficult to distinguish between a return value of <b>DDC_DEFAULT</b> and the error case, which is zero. To determine between the two, it is recommended that you call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError()</a> to check the error.

## -see-also

<a href="/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors">DIALOG_DPI_CHANGE_BEHAVIORS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior">SetDialogDpiChangeBehavior</a>