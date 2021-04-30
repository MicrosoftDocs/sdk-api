---
UID: NC:commdlg.LPSETUPHOOKPROC
title: LPSETUPHOOKPROC (commdlg.h)
description: An application-defined or library-defined callback function used with the PrintDlg function. The hook procedure receives messages or notifications intended for the default dialog box procedure of the Print Setup dialog box.
helpviewer_keywords: ["LPSETUPHOOKPROC","LPSETUPHOOKPROC callback","LPSETUPHOOKPROC callback function [Dialog Boxes]","_win32_SetupHookProc","_win32_setuphookproc_cpp","commdlg/LPSETUPHOOKPROC","dlgbox.setuphookproc","winui._win32_setuphookproc"]
old-location: dlgbox\setuphookproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\setuphookproc.htm
ms.date: 12/05/2018
ms.keywords: LPSETUPHOOKPROC, LPSETUPHOOKPROC callback, LPSETUPHOOKPROC callback function [Dialog Boxes], _win32_SetupHookProc, _win32_setuphookproc_cpp, commdlg/LPSETUPHOOKPROC, dlgbox.setuphookproc, winui._win32_setuphookproc
req.header: commdlg.h
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
 - LPSETUPHOOKPROC
 - commdlg/LPSETUPHOOKPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Commdlg.h
api_name:
 - LPSETUPHOOKPROC
---

## -description

An application-defined or library-defined callback function used with the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function. The hook procedure receives messages or notifications intended for the default dialog box procedure of the <b>Print Setup</b> dialog box.

The <b>LPSETUPHOOKPROC</b> type defines a pointer to this callback function. <i>SetupHookProc</i> is a placeholder for the application-defined or library-defined function name.

## -parameters

### -param unnamedParam1

A handle to the <b>Print Setup</b> dialog box for which the message is intended.

### -param unnamedParam2

The identifier of the message being received.

### -param unnamedParam3

Additional information about the message. The exact meaning depends on the value of the <i>unnamedParam2</i> parameter.

### -param unnamedParam4

Additional information about the message. The exact meaning depends on the value of the <i>unnamedParam2</i> parameter.

## -returns

If the hook procedure returns zero, the default dialog box procedure processes the message.

If the hook procedure returns a nonzero value, the default dialog box procedure ignores the message.

## -remarks

The <b>Print Setup</b> dialog box has been superseded by the <b>Page Setup</b> dialog box, which should be used by new applications. However, for compatibility, the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function continues to support display of the <b>Print Setup</b> dialog box. You can provide a <i>SetupHookProc</i> hook procedure for the <b>Print Setup</b> dialog box to process messages or notifications intended for the dialog box procedure.

To enable the hook procedure, use the <a href="/windows/win32/api/commdlg/ns-commdlg-printdlga">PRINTDLG</a> structure that you passed to the dialog creation function. Specify the address of the hook procedure in the  <b>lpfnSetupHook</b> member and specify the <b>PD_ENABLESETUPHOOK</b> flag in the  <b>Flags</b> member.

The default dialog box procedure processes the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message before passing it to the hook procedure. For all other messages, the hook procedure receives the message first. Then, the return value of the hook procedure determines whether the default dialog procedure processes the message or ignores it.

If the hook procedure processes the <a href="/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to painting the background of the dialog box. In general, if the hook procedure processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to painting the background of the specified control.

Do not call the <a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function from the hook procedure. Instead, the hook procedure can call the <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function to post a  <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message with the <b>IDABORT</b> value to the dialog box procedure. Posting <b>IDABORT</b> closes the dialog box and causes the dialog box function to return <b>FALSE</b>. If you need to know why the hook procedure closed the dialog box, you must provide your own communication mechanism between the hook procedure and your application.

You can subclass the standard controls of a common dialog box. However, the dialog box procedure may also subclass the controls. Because of this, you should subclass controls when your hook procedure processes the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. This ensures that your subclass procedure receives the control-specific messages before the subclass procedure set by the dialog box procedure.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a>



<a href="/windows/win32/api/commdlg/ns-commdlg-printdlga">PRINTDLG</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a>



<b>Reference</b>



<a href="/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>