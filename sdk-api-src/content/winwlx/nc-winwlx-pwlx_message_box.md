---
UID: NC:winwlx.PWLX_MESSAGE_BOX
title: PWLX_MESSAGE_BOX (winwlx.h)
description: Called by GINA to create, display, and operate a message box.
helpviewer_keywords: ["MB_ABORTRETRYIGNORE","MB_APPLMODAL","MB_DEFAULT_DESKTOP_ONLY","MB_DEFBUTTON1","MB_DEFBUTTON2","MB_DEFBUTTON3","MB_DEFBUTTON4","MB_ICONASTERISK","MB_ICONEXCLAMATION","MB_ICONHAND","MB_ICONINFORMATION","MB_ICONQUESTION","MB_ICONSTOP","MB_OK","MB_OKCANCEL","MB_RETRYCANCEL","MB_SERVICE_NOTIFICATION","MB_SETFOREGROUND","MB_SYSTEMMODAL","MB_TASKMODAL","MB_YESNO","MB_YESNOCANCEL","PWLX_MESSAGE_BOX","PWLX_MESSAGE_BOX callback","WlxMessageBox","WlxMessageBox callback function [Security]","_gina_wlxmessagebox","security.wlxmessagebox","winwlx/WlxMessageBox"]
old-location: security\wlxmessagebox.htm
tech.root: security
ms.assetid: 5ae99416-c502-46f6-ba58-7385ce410e48
ms.date: 12/05/2018
ms.keywords: MB_ABORTRETRYIGNORE, MB_APPLMODAL, MB_DEFAULT_DESKTOP_ONLY, MB_DEFBUTTON1, MB_DEFBUTTON2, MB_DEFBUTTON3, MB_DEFBUTTON4, MB_ICONASTERISK, MB_ICONEXCLAMATION, MB_ICONHAND, MB_ICONINFORMATION, MB_ICONQUESTION, MB_ICONSTOP, MB_OK, MB_OKCANCEL, MB_RETRYCANCEL, MB_SERVICE_NOTIFICATION, MB_SETFOREGROUND, MB_SYSTEMMODAL, MB_TASKMODAL, MB_YESNO, MB_YESNOCANCEL, PWLX_MESSAGE_BOX, PWLX_MESSAGE_BOX callback, WlxMessageBox, WlxMessageBox callback function [Security], _gina_wlxmessagebox, security.wlxmessagebox, winwlx/WlxMessageBox
req.header: winwlx.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWLX_MESSAGE_BOX
 - winwlx/PWLX_MESSAGE_BOX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxMessageBox
---

# PWLX_MESSAGE_BOX callback function


## -description

<p class="CCE_Message">[The WlxMessageBox function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxMessageBox</b> function is called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to create, display, and operate a message box.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param hwndOwner [in]

Specifies the owner window of the message box to be created. If this parameter is <b>NULL</b>, the message box has no owner window.

### -param lpszText [in]

Points to a null-terminated string that contains the message to be displayed.

### -param lpszTitle [in]

Points to a null-terminated string used for the dialog box title. If this parameter is <b>NULL</b>, the default title Error is used.

### -param fuStyle [in]

Specifies the content and behavior of the dialog box. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MB_ABORTRETRYIGNORE"></a><a id="mb_abortretryignore"></a><dl>
<dt><b>MB_ABORTRETRYIGNORE</b></dt>
</dl>
</td>
<td width="60%">
The message box contains three command buttons: <b>Abort</b>, <b>Retry</b>, and <b>Ignore</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_APPLMODAL"></a><a id="mb_applmodal"></a><dl>
<dt><b>MB_APPLMODAL</b></dt>
</dl>
</td>
<td width="60%">
The user must respond to the message box before continuing to work in the window identified by the <i>hWndOwner</i> parameter. However, the user can move to windows of other applications to work. 




Depending on the hierarchy of windows in the application, the user may be able to move to other windows within the application. All child windows of the parent of the message box are automatically disabled but pop-up windows are not.

MB_APPLMODAL is the default value if neither MB_SYSTEMMODAL nor MB_TASKMODAL is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_DEFAULT_DESKTOP_ONLY"></a><a id="mb_default_desktop_only"></a><dl>
<dt><b>MB_DEFAULT_DESKTOP_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The desktop currently receiving input must be a default desktop; otherwise, the function fails. A default desktop is one on which an application runs after the user has logged on.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_DEFBUTTON1"></a><a id="mb_defbutton1"></a><dl>
<dt><b>MB_DEFBUTTON1</b></dt>
</dl>
</td>
<td width="60%">
The first button is the default button. Note that the first button is always the default unless MB_DEFBUTTON2 or MB_DEFBUTTON3 is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_DEFBUTTON2"></a><a id="mb_defbutton2"></a><dl>
<dt><b>MB_DEFBUTTON2</b></dt>
</dl>
</td>
<td width="60%">
The second button is a default button.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_DEFBUTTON3"></a><a id="mb_defbutton3"></a><dl>
<dt><b>MB_DEFBUTTON3</b></dt>
</dl>
</td>
<td width="60%">
The third button is a default button.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_DEFBUTTON4"></a><a id="mb_defbutton4"></a><dl>
<dt><b>MB_DEFBUTTON4</b></dt>
</dl>
</td>
<td width="60%">
The fourth button is a default button.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONASTERISK"></a><a id="mb_iconasterisk"></a><dl>
<dt><b>MB_ICONASTERISK</b></dt>
</dl>
</td>
<td width="60%">
An icon that consists of a lowercase letter in a circle appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONEXCLAMATION"></a><a id="mb_iconexclamation"></a><dl>
<dt><b>MB_ICONEXCLAMATION</b></dt>
</dl>
</td>
<td width="60%">
An exclamation point icon appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONHAND"></a><a id="mb_iconhand"></a><dl>
<dt><b>MB_ICONHAND</b></dt>
</dl>
</td>
<td width="60%">
A hand icon appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONINFORMATION"></a><a id="mb_iconinformation"></a><dl>
<dt><b>MB_ICONINFORMATION</b></dt>
</dl>
</td>
<td width="60%">
An icon that consists of a lowercase letter in a circle appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONQUESTION"></a><a id="mb_iconquestion"></a><dl>
<dt><b>MB_ICONQUESTION</b></dt>
</dl>
</td>
<td width="60%">
A question mark icon appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ICONSTOP"></a><a id="mb_iconstop"></a><dl>
<dt><b>MB_ICONSTOP</b></dt>
</dl>
</td>
<td width="60%">
A stop sign icon appears in the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_OK"></a><a id="mb_ok"></a><dl>
<dt><b>MB_OK</b></dt>
</dl>
</td>
<td width="60%">
The message box contains one command button: <b>OK</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_OKCANCEL"></a><a id="mb_okcancel"></a><dl>
<dt><b>MB_OKCANCEL</b></dt>
</dl>
</td>
<td width="60%">
The message box contains two command buttons: <b>OK</b> and <b>Cancel</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_RETRYCANCEL"></a><a id="mb_retrycancel"></a><dl>
<dt><b>MB_RETRYCANCEL</b></dt>
</dl>
</td>
<td width="60%">
The message box contains two command buttons: <b>Retry</b> and <b>Cancel</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_SERVICE_NOTIFICATION"></a><a id="mb_service_notification"></a><dl>
<dt><b>MB_SERVICE_NOTIFICATION</b></dt>
</dl>
</td>
<td width="60%">
The caller is a service notifying the user of an event. The function brings up a message box on the current active desktop, even if there is no user logged on to the computer.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_SETFOREGROUND"></a><a id="mb_setforeground"></a><dl>
<dt><b>MB_SETFOREGROUND</b></dt>
</dl>
</td>
<td width="60%">
The message box becomes the foreground window. Internally, Windows calls the 
<a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> function for the message box.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_SYSTEMMODAL"></a><a id="mb_systemmodal"></a><dl>
<dt><b>MB_SYSTEMMODAL</b></dt>
</dl>
</td>
<td width="60%">
All applications are suspended until the user responds to the message box. Unless the application specifies MB_ICONHAND, the message box does not become modal until after it is created. Consequently, the owner window and other windows continue to receive messages resulting from its activation. Use system-modal message boxes to notify the user of serious, potentially damaging errors that require immediate attention, for example, running out of memory.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_TASKMODAL"></a><a id="mb_taskmodal"></a><dl>
<dt><b>MB_TASKMODAL</b></dt>
</dl>
</td>
<td width="60%">
Same as MB_APPLMODAL except that all the top-level windows that belong to the current task are disabled if the <i>hWndOwner</i> parameter is <b>NULL</b>. Use this flag when the calling application or library does not have a window handle available, but still needs to prevent input to other windows in the current application without suspending other applications.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_YESNO"></a><a id="mb_yesno"></a><dl>
<dt><b>MB_YESNO</b></dt>
</dl>
</td>
<td width="60%">
The message box contains two command buttons: <b>Yes</b> and <b>No</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_YESNOCANCEL"></a><a id="mb_yesnocancel"></a><dl>
<dt><b>MB_YESNOCANCEL</b></dt>
</dl>
</td>
<td width="60%">
The message box contains three command buttons: <b>Yes</b>, <b>No</b>, and <b>Cancel</b>.

</td>
</tr>
</table>

## -returns

If the function fails, or if there is not enough memory to create the message box, the return value is zero.

If the function succeeds, the return value is one of the following menu item values returned by the dialog box.

<div class="alert"><b>Note</b>  If a message box has a <b>Cancel</b> button, the function returns the IDCANCEL value if either the <b>ESC</b> key is pressed or the <b>Cancel</b> button is clicked. If the message box has no <b>Cancel</b> button, pressing <b>ESC</b> has no effect.</div>
<div> </div>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDABORT</b></dt>
</dl>
</td>
<td width="60%">
<b>Abort</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDCANCEL</b></dt>
</dl>
</td>
<td width="60%">
<b>Cancel</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDIGNORE</b></dt>
</dl>
</td>
<td width="60%">
<b>Ignore</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDNO</b></dt>
</dl>
</td>
<td width="60%">
A  button was not selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDOK</b></dt>
</dl>
</td>
<td width="60%">
<b>OK</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDRETRY</b></dt>
</dl>
</td>
<td width="60%">
<b>Retry</b> button was selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDYES</b></dt>
</dl>
</td>
<td width="60%">
<b>Yes</b> button was selected.

</td>
</tr>
</table>

## -remarks

The <b>WlxMessageBox</b> function does not handle <a href="/windows/desktop/SecGloss/s-gly">SAS</a> events, and is not suitable for security dialog boxes. Use the 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box">WlxDialogBox</a>, 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect">WlxDialogBoxIndirect</a>, or 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param">WlxDialogBoxIndirectParam</a> function for security dialog boxes.

<b>WlxMessageBox</b> duplicates the Windows 
<a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> function, with the exception that this function also allows Winlogon to time out the dialog box. For more information, see 
<b>MessageBox</b>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box">WlxDialogBox</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect">WlxDialogBoxIndirect</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param">WlxDialogBoxIndirectParam</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>