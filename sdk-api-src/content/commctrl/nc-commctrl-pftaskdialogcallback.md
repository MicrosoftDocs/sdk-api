---
UID: NC:commctrl.PFTASKDIALOGCALLBACK
title: PFTASKDIALOGCALLBACK (commctrl.h)
description: The TaskDialogCallbackProc function is an application-defined function used with the TaskDialogIndirect function.
helpviewer_keywords: ["PFTASKDIALOGCALLBACK","PFTASKDIALOGCALLBACK callback","PFTASKDIALOGCALLBACK callback function [Windows Controls]","_shell_TaskDialogCallbackProc","_shell_TaskDialogCallbackProc_cpp","commctrl/PFTASKDIALOGCALLBACK","controls.TaskDialogCallbackProc","controls._shell_TaskDialogCallbackProc"]
old-location: controls\TaskDialogCallbackProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\taskdialogs\taskdialogreference\taskdialogfunctions\taskdialogcallbackproc.htm
ms.date: 12/05/2018
ms.keywords: PFTASKDIALOGCALLBACK, PFTASKDIALOGCALLBACK callback, PFTASKDIALOGCALLBACK callback function [Windows Controls], _shell_TaskDialogCallbackProc, _shell_TaskDialogCallbackProc_cpp, commctrl/PFTASKDIALOGCALLBACK, controls.TaskDialogCallbackProc, controls._shell_TaskDialogCallbackProc
req.header: commctrl.h
req.include-header: Commctrl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PFTASKDIALOGCALLBACK
 - commctrl/PFTASKDIALOGCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Commctrl.h
api_name:
 - PFTASKDIALOGCALLBACK
---

## -description

The <i>TaskDialogCallbackProc</i> function is an application-defined function used with the <a href="/windows/desktop/api/commctrl/nf-commctrl-taskdialogindirect">TaskDialogIndirect</a> function. It receives messages from the task dialog when various events occur.

The <b>PFTASKDIALOGCALLBACK</b> type defines a pointer to this callback function. <i>TaskDialogCallbackProc</i> is a placeholder for the application defined function name.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the TaskDialog window. Do not continue sending messages to hwnd after the callback procedure returns from having been called with <a href="/windows/desktop/Controls/tdn-destroyed">TDN_DESTROYED</a>.

### -param msg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

One of the following notifications.

<table class="clsStd">
<tr>
<th>Notification</th>
<th>Usage</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-button-clicked">TDN_BUTTON_CLICKED</a>
</td>
<td>Indicates that a button has been selected. The command ID of the button is specified by <i>wParam</i>.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-created">TDN_CREATED</a>
</td>
<td>Indicates that the Task Dialog has been created.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-destroyed">TDN_DESTROYED</a>
</td>
<td>Indicates that the Task Dialog has been destroyed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-dialog-constructed">TDN_DIALOG_CONSTRUCTED</a>
</td>
<td>Indicates that the Task Dialog has been created but has not been displayed yet.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-expando-button-clicked">TDN_EXPANDO_BUTTON_CLICKED</a>
</td>
<td>Indicates that the expando button has been selected.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-help">TDN_HELP</a>
</td>
<td>Indicates that the F1 key has been pressed while the Task Dialog has focus.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-hyperlink-clicked">TDN_HYPERLINK_CLICKED</a>
</td>
<td>Indicates that a hyperlink has been selected. A pointer to the link text is specified by <i>lParam</i>.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-navigated">TDN_NAVIGATED</a>
</td>
<td>Indicates that navigation has occurred.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-radio-button-clicked">TDN_RADIO_BUTTON_CLICKED</a>
</td>
<td>Indicates that a radio button has been selected. The command ID of the radio button is specified by <i>wParam</i>.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-timer">TDN_TIMER</a>
</td>
<td>Indicates that the Task Dialog timer has fired. The total elapsed time is specified by <i>wParam</i>. You can update the progress bar by sending a <a href="/windows/desktop/Controls/tdm-set-progress-bar-pos">TDM_SET_PROGRESS_BAR_POS</a> message to the window specified by the <i>hwnd</i> parameter.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/tdn-verification-clicked">TDN_VERIFICATION_CLICKED</a>
</td>
<td>Indicates that the Task Dialog verification check box has been selected.</td>
</tr>
</table>

### -param wParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

Specifies additional notification information.  The contents of this parameter depend on the value of the <i>uNotification</i> parameter.

### -param lParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Specifies additional notification information.  The contents of this parameter depend on the value of the <i>uNotification</i> parameter.

### -param lpRefData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG_PTR</a></b>

Pointer to application specific data. This is the data pointed to by the <b>lpCallbackData</b> member of structure <a href="/windows/desktop/api/commctrl/ns-commctrl-taskdialogconfig">TASKDIALOGCONFIG</a> used to create the task dialog.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is specific to the notification being processed. When responding to a button click, your implementation should return S_FALSE if the Task Dialog is not to close. Otherwise return S_OK.

## -remarks

An application must register this callback function by passing its address in the <b>pfCallback</b> member of  the <a href="/windows/desktop/api/commctrl/ns-commctrl-taskdialogconfig">TASKDIALOGCONFIG</a> structure that is passed via pointer through <a href="/windows/desktop/api/commctrl/nf-commctrl-taskdialogindirect">TaskDialogIndirect</a>.