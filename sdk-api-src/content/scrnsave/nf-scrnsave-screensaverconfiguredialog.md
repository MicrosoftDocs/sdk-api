---
UID: NF:scrnsave.ScreenSaverConfigureDialog
title: ScreenSaverConfigureDialog function (scrnsave.h)
description: Receives messages sent to a screen saver's configuration dialog box. A screen saver that allows user configuration must define this function.
helpviewer_keywords: ["ScreenSaverConfigureDialog","ScreenSaverConfigureDialog function [Windows Shell]","_win32_ScreenSaverConfigureDialog","scrnsave/ScreenSaverConfigureDialog","shell.ScreenSaverConfigureDialog"]
old-location: shell\ScreenSaverConfigureDialog.htm
tech.root: shell
ms.assetid: 84c2966f-8f01-4f8d-9cec-c7fef657bff0
ms.date: 12/05/2018
ms.keywords: ScreenSaverConfigureDialog, ScreenSaverConfigureDialog function [Windows Shell], _win32_ScreenSaverConfigureDialog, scrnsave/ScreenSaverConfigureDialog, shell.ScreenSaverConfigureDialog
req.header: scrnsave.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Scrnsave.lib
req.dll: None
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScreenSaverConfigureDialog
 - scrnsave/ScreenSaverConfigureDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - ScreenSaverConfigureDialog
---

# ScreenSaverConfigureDialog function


## -description

Receives messages sent to a screen saver's configuration dialog box. A screen saver that allows user configuration must define this function.

## -parameters

### -param hDlg

Type: <b>HWND</b>

The identifier of the configuration dialog box.

### -param message

Type: <b>UINT</b>

A message that was sent to the screen saver's configuration dialog box.

### -param wParam

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>BOOL</b>

If the function successfully processes the message, it should return <b>TRUE</b>. If not, it should return <b>FALSE</b>, except in response to a <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. In response to a <b>WM_INITDIALOG</b> message, <b>ScreenSaverConfigureDialog</b> should return <b>FALSE</b> if it calls the <a href="/windows/desktop/api/winuser/nf-winuser-setfocus">SetFocus</a> function to set the keyboard focus to one of the controls in the dialog box. Otherwise, the function should return <b>TRUE</b>, in which case the system sets the keyboard focus to the first control in the dialog box that can be given the focus.

## -remarks

The dialog box template for the configuration dialog box must have the <b>DLG_SCRNSAVECONFIGURE</b> identifier.

The dialog box procedure is used only if the application specifies the default window class (<b>WC_DIALOG</b>) for the dialog box. The application uses the default class if no explicit class is given in the dialog box template. Although the dialog box procedure is similar to a window procedure, it must not call the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to process unwanted messages. Unwanted messages are processed internally by the default dialog box procedure.

The <b>ScreenSaverConfigureDialog</b> function must be exported by including it in the EXPORTS statement in the application's module-definition (.def) file.

## -see-also

<a href="/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses">RegisterDialogClasses</a>