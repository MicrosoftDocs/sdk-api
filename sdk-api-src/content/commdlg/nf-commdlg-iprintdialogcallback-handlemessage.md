---
UID: NF:commdlg.IPrintDialogCallback.HandleMessage
title: IPrintDialogCallback::HandleMessage (commdlg.h)
description: Called by PrintDlgEx to give your application an opportunity to handle messages sent to the child dialog box in the lower portion of the General page of the Print Property Sheet.
helpviewer_keywords: ["HandleMessage","HandleMessage method [Dialog Boxes]","HandleMessage method [Dialog Boxes]","IPrintDialogCallback interface","IPrintDialogCallback interface [Dialog Boxes]","HandleMessage method","IPrintDialogCallback.HandleMessage","IPrintDialogCallback::HandleMessage","_win32_IPrintDialogCallback_HandleMessage","_win32_iprintdialogcallback_handlemessage_cpp","commdlg/IPrintDialogCallback::HandleMessage","dlgbox.iprintdialogcallback_handlemessage","winui._win32_iprintdialogcallback_handlemessage"]
old-location: dlgbox\iprintdialogcallback_handlemessage.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogcallback\iprintdialogcallbackhandlemessage.htm
ms.date: 12/05/2018
ms.keywords: HandleMessage, HandleMessage method [Dialog Boxes], HandleMessage method [Dialog Boxes],IPrintDialogCallback interface, IPrintDialogCallback interface [Dialog Boxes],HandleMessage method, IPrintDialogCallback.HandleMessage, IPrintDialogCallback::HandleMessage, _win32_IPrintDialogCallback_HandleMessage, _win32_iprintdialogcallback_handlemessage_cpp, commdlg/IPrintDialogCallback::HandleMessage, dlgbox.iprintdialogcallback_handlemessage, winui._win32_iprintdialogcallback_handlemessage
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
req.dll: Comdlg32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintDialogCallback::HandleMessage
 - commdlg/IPrintDialogCallback::HandleMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IPrintDialogCallback.HandleMessage
---

# IPrintDialogCallback::HandleMessage


## -description

Called by <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> to give your application an opportunity to handle messages sent to the child dialog box in the lower portion of the <b>General</b> page of the <a href="/windows/desktop/dlgbox/print-property-sheet">Print Property Sheet</a>. The child dialog box contains controls similar to those of the <b>Print</b> dialog box.

## -parameters

### -param hDlg

Type: <b>HWND</b>

A handle to the child dialog box in the lower portion of the <b>General</b> page.

### -param uMsg

Type: <b>UINT</b>

The identifier of the message being received.

### -param wParam

Type: <b>WPARAM</b>

Additional information about the message. The exact meaning depends on the value of the <i>uMsg</i> parameter.

### -param lParam

Type: <b>LPARAM</b>

Additional information about the message. The exact meaning depends on the value of the <i>uMsg</i> parameter.

					

If the <i>uMsg</i> parameter indicates the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message, <i>lParam</i> is a pointer to a <a href="/windows/win32/api/commdlg/ns-commdlg-printdlgexa">PRINTDLGEX</a> structure containing the values specified when the property sheet was created.

### -param pResult

Type: <b>LRESULT*</b>

Indicates the result to be returned by the dialog box procedure for the message. The value pointed to should be <b>TRUE</b> if you process the message, otherwise it should be <b>FALSE</b> or whatever is an appropriate value according to the message type.

## -returns

Type: <b>HRESULT</b>

Return <b>S_OK</b> if your <b>IPrintDialogCallback::HandleMessage</b> implementation handled the message. In this case, the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function does not perform any default message handling.

Return <b>S_FALSE</b> if you want <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> to perform its default message handling.

## -remarks

For notification messages passed by the <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message, you must use the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a> function with the <b>DWL_MSGRESULT</b> value to set a return value. When you call <b>SetWindowLong</b>, use <a href="/windows/desktop/api/winuser/nf-winuser-getparent">GetParent</a>(<i>hDlg</i>) to set the <b>DWL_MSGRESULT</b> value of the <b>General</b> page, which is the parent of the child window.

The default dialog box procedure for the child window in the lower portion of the <b>General</b> page processes the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message before passing it to the <b>HandleMessage</b> method. For all other messages sent to the child window, <b>HandleMessage</b> receives the message first. Then the <b>HandleMessage</b> return value determines whether the default dialog procedure processes the message or ignores it.

If <b>HandleMessage</b> processes the <a href="/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a> message, it must return a valid brush handle to painting the background of the dialog box. In general, if <b>HandleMessage</b> processes any <b>WM_CTLCOLOR*</b> message, it must return a valid brush handle to painting the background of the specified control.

Do not call the <a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function from the <b>HandleMessage</b> method. Instead, <b>HandleMessage</b> can call the <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function to post a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message with the IDABORT value to the dialog box procedure. Posting <b>IDABORT</b> closes the <a href="/windows/desktop/dlgbox/print-property-sheet">Print Property Sheet</a> and causes <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> to return <b>PD_RESULT_CANCEL</b> in the <b>dwResultAction</b> member of the <a href="/windows/win32/api/commdlg/ns-commdlg-printdlgexa">PRINTDLGEX</a> structure. If you need to know why <b>HandleMessage</b> closed the dialog box, you must provide your own communication mechanism between the <b>HandleMessage</b> method and your application.

You can subclass the standard controls of the child dialog box in the lower portion of the <b>General</b> page. These standard controls are similar to those found in the <b>Print</b> dialog box. However, the default dialog box procedure may also subclass the controls. Because of this, you should subclass controls when <b>HandleMessage</b> processes the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. This ensures that your subclass procedure receives control-specific messages before the subclass procedure set by the dialog box procedure.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogcallback">IPrintDialogCallback</a>



<b>Other Resources</b>



<a href="/windows/win32/api/commdlg/ns-commdlg-printdlgexa">PRINTDLGEX</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>



<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>



<a href="/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>



<a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>