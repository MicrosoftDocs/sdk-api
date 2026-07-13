---
UID: NC:winuser.DLGPROC
title: DLGPROC (winuser.h)
description: Application-defined callback function used with the CreateDialog and DialogBox families of functions.
helpviewer_keywords: ["DLGPROC","DLGPROC callback","DLGPROC callback function [Dialog Boxes]","_win32_DialogProc","_win32_dialogproc_cpp","dlgbox.dialogproc","winui._win32_dialogproc","winuser/DLGPROC"]
old-location: dlgbox\dialogproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogproc.htm
ms.date: 09/30/2025
ms.keywords: DLGPROC, DLGPROC callback, DLGPROC callback function [Dialog Boxes], _win32_DialogProc, _win32_dialogproc_cpp, dlgbox.dialogproc, winui._win32_dialogproc, winuser/DLGPROC
req.header: winuser.h
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
 - DLGPROC
 - winuser/DLGPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - DLGPROC
---

# DLGPROC callback function

## -description

Application-defined callback function used with the [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialoga) and [DialogBox](/windows/desktop/api/winuser/nf-winuser-dialogboxa) families of functions. It processes messages sent to a modal or modeless dialog box. The **DLGPROC** type defines a pointer to this callback function. _DialogProc_ is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: **HWND**

A handle to the dialog box. This parameter is typically named _hWnd_.

### -param unnamedParam2

Type: **UINT**

The message. This parameter is typically named _uMsg_.

### -param unnamedParam3

Type: **WPARAM**

Additional message-specific information. This parameter is typically named _wParam_.

### -param unnamedParam4

Type: **LPARAM**

Additional message-specific information. This parameter is typically named _lParam_.

## -returns

Type: **INT_PTR**

Typically, the dialog box procedure should return **TRUE** if it processed the message, and **FALSE** if it did not. If the dialog box procedure returns **FALSE**, the dialog manager performs the default dialog operation in response to the message.

If the dialog box procedure processes a message that requires a specific return value, the dialog box procedure should set the desired return value by calling [SetWindowLong](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)(_hwndDlg_, **DWL_MSGRESULT**, _lResult_) immediately before returning **TRUE**. Note that you must call **SetWindowLong** immediately before returning **TRUE**; doing so earlier may result in the **DWL_MSGRESULT** value being overwritten by a nested dialog box message.

The following messages are exceptions to the general rules stated above. Consult the documentation for the specific message for details on the semantics of the return value.

- [WM_CHARTOITEM](/windows/desktop/Controls/wm-chartoitem)
- [WM_COMPAREITEM](/windows/desktop/Controls/wm-compareitem)
- [WM_CTLCOLORBTN](/windows/desktop/Controls/wm-ctlcolorbtn)
- [WM_CTLCOLORDLG](/windows/desktop/dlgbox/wm-ctlcolordlg)
- [WM_CTLCOLOREDIT](/windows/desktop/Controls/wm-ctlcoloredit)
- [WM_CTLCOLORLISTBOX](/windows/desktop/Controls/wm-ctlcolorlistbox)
- [WM_CTLCOLORSCROLLBAR](/windows/desktop/Controls/wm-ctlcolorscrollbar)
- [WM_CTLCOLORSTATIC](/windows/desktop/Controls/wm-ctlcolorstatic)
- [WM_INITDIALOG](/windows/desktop/dlgbox/wm-initdialog)
- [WM_QUERYDRAGICON](/windows/desktop/winmsg/wm-querydragicon)
- [WM_VKEYTOITEM](/windows/desktop/Controls/wm-vkeytoitem)

## -remarks

> [!NOTE]
> The parameters are defined in the header with no names: `typedef INT_PTR (CALLBACK* DLGPROC)(HWND, UINT, WPARAM, LPARAM);`. Therefore, the syntax block lists them as `unnamedParam1` - `unnamedParam4`. You can name these parameters anything in your app. However, they are usually named as shown in the parameter descriptions.

You should use the dialog box procedure only if you use the dialog box class for the dialog box. This is the default class and is used when no explicit class is specified in the dialog box template. Although the dialog box procedure is similar to a window procedure, it must not call the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function to process unwanted messages. Unwanted messages are processed internally by the dialog box window procedure.

## -see-also

**Conceptual**

[Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes)

[WM_INITDIALOG](/windows/desktop/dlgbox/wm-initdialog)

**Reference**

[CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialoga)

[CreateDialogIndirect](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta)

[CreateDialogIndirectParam](/windows/desktop/api/winuser/nf-winuser-createdialogindirectparama)

[CreateDialogParam](/windows/desktop/api/winuser/nf-winuser-createdialogparama)

[DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

[DialogBox](/windows/desktop/api/winuser/nf-winuser-dialogboxa)

[DialogBoxIndirect](/windows/desktop/api/winuser/nf-winuser-dialogboxindirecta)

[DialogBoxIndirectParam](/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama)

[DialogBoxParam](/windows/desktop/api/winuser/nf-winuser-dialogboxparama)

[SetFocus](/windows/desktop/api/winuser/nf-winuser-setfocus)