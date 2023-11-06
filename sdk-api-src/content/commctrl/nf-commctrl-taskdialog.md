---
UID: NF:commctrl.TaskDialog
title: TaskDialog function (commctrl.h)
description: The TaskDialog function creates, displays, and operates a task dialog.
helpviewer_keywords: ["TDCBF_CANCEL_BUTTON","TDCBF_CLOSE_BUTTON","TDCBF_NO_BUTTON","TDCBF_OK_BUTTON","TDCBF_RETRY_BUTTON","TDCBF_YES_BUTTON","TD_ERROR_ICON","TD_INFORMATION_ICON","TD_SHIELD_ICON","TD_WARNING_ICON","TaskDialog","TaskDialog function [Windows Controls]","_shell_TaskDialog","_shell_TaskDialog_cpp","commctrl/TaskDialog","controls.TaskDialog","controls._shell_TaskDialog"]
old-location: controls\TaskDialog.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\taskdialogs\taskdialogreference\taskdialogfunctions\taskdialog.htm
ms.date: 12/05/2018
ms.keywords: TDCBF_CANCEL_BUTTON, TDCBF_CLOSE_BUTTON, TDCBF_NO_BUTTON, TDCBF_OK_BUTTON, TDCBF_RETRY_BUTTON, TDCBF_YES_BUTTON, TD_ERROR_ICON, TD_INFORMATION_ICON, TD_SHIELD_ICON, TD_WARNING_ICON, TaskDialog, TaskDialog function [Windows Controls], _shell_TaskDialog, _shell_TaskDialog_cpp, commctrl/TaskDialog, controls.TaskDialog, controls._shell_TaskDialog
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 6)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TaskDialog
 - commctrl/TaskDialog
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
 - TaskDialog
---

# TaskDialog function


## -description

The <b>TaskDialog</b> function creates, displays, and operates a task dialog. The task dialog contains application-defined message text and title, icons, and any combination of predefined push buttons. This function does not support the registration of a callback function to receive notifications.

## -parameters

### -param hwndOwner [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the owner window of the task dialog to be created. If this parameter is <b>NULL</b>, the task dialog has no owner window.

### -param hInstance [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the module that contains the icon resource identified by the <i>pszIcon</i> member, and the string resources identified by the <i>pszWindowTitle</i> and <i>pszMainInstruction</i> members.  If this parameter is <b>NULL</b>, <i>pszIcon</i> must be <b>NULL</b> or a pointer to a null-terminated, Unicode string that contains a system resource identifier, for example, TD_ERROR_ICON.

### -param pszWindowTitle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PCWSTR</a></b>

Pointer to the string to be used for the task dialog title. This parameter is a null-terminated, Unicode string that contains either text, or an integer resource identifier passed through the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro.  If this parameter is <b>NULL</b>, the filename of the executable program is used.

### -param pszMainInstruction [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PCWSTR</a></b>

Pointer to the string to be used for the main instruction. This parameter is a null-terminated, Unicode string that contains either text, or an integer resource identifier passed through the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro.  This parameter can be <b>NULL</b> if no main instruction is wanted.

### -param pszContent [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PCWSTR</a></b>

Pointer to a string used for additional text that appears below the main instruction, in a smaller font. This parameter is a null-terminated, Unicode string that contains either text, or an integer resource identifier passed through the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. Can be <b>NULL</b> if no additional text is wanted.

### -param dwCommonButtons [in]

Type: <b>TASKDIALOG_COMMON_BUTTON_FLAGS</b>

Specifies the push buttons displayed in the dialog box. This parameter may be a combination of flags from the following group.

<div class="alert"><b>Note</b>  If no buttons are specified, the dialog box will contain the <b>OK</b> button by default.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TDCBF_OK_BUTTON"></a><a id="tdcbf_ok_button"></a><dl>
<dt><b>TDCBF_OK_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
The task dialog contains the push button: <b>OK</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TDCBF_YES_BUTTON"></a><a id="tdcbf_yes_button"></a><dl>
<dt><b>TDCBF_YES_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
The task dialog contains the push button: <b>Yes</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TDCBF_NO_BUTTON"></a><a id="tdcbf_no_button"></a><dl>
<dt><b>TDCBF_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
The task dialog contains the push button: <b>No</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TDCBF_CANCEL_BUTTON"></a><a id="tdcbf_cancel_button"></a><dl>
<dt><b>TDCBF_CANCEL_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
The task dialog contains the push button: <b>Cancel</b>. This button must be specified for the dialog box to respond to typical cancel actions (Alt-F4 and Escape).

</td>
</tr>
<tr>
<td width="40%"><a id="TDCBF_RETRY_BUTTON"></a><a id="tdcbf_retry_button"></a><dl>
<dt><b>TDCBF_RETRY_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
The task dialog contains the push button: <b>Retry</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TDCBF_CLOSE_BUTTON"></a><a id="tdcbf_close_button"></a><dl>
<dt><b>TDCBF_CLOSE_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
The task dialog contains the push button: <b>Close</b>.

</td>
</tr>
</table>

### -param pszIcon [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PCWSTR</a></b>

Pointer to a string that identifies the icon to display in the task dialog. This parameter must be an integer resource identifier passed to the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro or one of the following predefined values. If this parameter is <b>NULL</b>, no icon will be displayed. If the <i>hInstance</i> parameter is <b>NULL</b> and one of the predefined values is not used, the <b>TaskDialog</b> function fails.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TD_ERROR_ICON"></a><a id="td_error_icon"></a><dl>
<dt><b>TD_ERROR_ICON</b></dt>
</dl>
</td>
<td width="60%">
A stop-sign icon appears in the task dialog.

</td>
</tr>
<tr>
<td width="40%"><a id="TD_INFORMATION_ICON"></a><a id="td_information_icon"></a><dl>
<dt><b>TD_INFORMATION_ICON</b></dt>
</dl>
</td>
<td width="60%">
An icon consisting of a lowercase letter i in a circle appears in the task dialog.

</td>
</tr>
<tr>
<td width="40%"><a id="TD_SHIELD_ICON"></a><a id="td_shield_icon"></a><dl>
<dt><b>TD_SHIELD_ICON</b></dt>
</dl>
</td>
<td width="60%">
A security shield icon appears in the task dialog.


</td>
</tr>
<tr>
<td width="40%"><a id="TD_WARNING_ICON"></a><a id="td_warning_icon"></a><dl>
<dt><b>TD_WARNING_ICON</b></dt>
</dl>
</td>
<td width="60%">
An exclamation-point icon appears in the task dialog.

</td>
</tr>
</table>

### -param pnButton [out]

Type: <b>int*</b>

When this function returns, contains a pointer to an integer location that receives one of the following values:

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Function call failed. Refer to return value for more information.</td>
</tr>
<tr>
<td><b>IDCANCEL</b></td>
<td><b>Cancel</b> button was selected, Alt-F4 was pressed, Escape was pressed or the user clicked on the <b>close window</b> button.</td>
</tr>
<tr>
<td><b>IDNO</b></td>
<td><b>No</b> button was selected.</td>
</tr>
<tr>
<td><b>IDOK</b></td>
<td><b>OK</b> button was selected.</td>
</tr>
<tr>
<td><b>IDRETRY</b></td>
<td><b>Retry</b> button was selected.</td>
</tr>
<tr>
<td><b>IDYES</b></td>
<td><b>Yes</b> button was selected.</td>
</tr>
<tr>
<td><b>IDCLOSE</b></td>
<td><b>Close</b> button was selected.</td>
</tr>
</table>
 

If this value is <b>NULL</b>, no value is returned.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>

## -remarks

When you use a task dialog box to indicate that the system is low on memory, the strings pointed to by the <i>pszMainInstruction</i> and <i>pszWindowTitle</i> parameters should not be taken from a resource file since an attempt to load the resource may fail. 

 If you create a task dialog while a dialog box is present, use a handle to the dialog box as the <i>hWndParent</i> parameter. The <i>hWndParent</i> parameter should not identify a child window, such as a control in a dialog box. 

Because task dialog boxes use the correct system-defined UI elements, you should use them instead of using message boxes created with the <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> function. To achieve more functionality, use <a href="/windows/desktop/api/commctrl/nf-commctrl-taskdialogindirect">TaskDialogIndirect</a>.

The following example code, to be included as part of a larger program, shows how to create a task dialog and capture input.
			
			


```

int nButtonPressed = 0;
TaskDialog(NULL, hInst, 
    MAKEINTRESOURCE(IDS_APPLICATION_TITLE),
    MAKEINTRESOURCE(IDS_DOSOMETHING), 
    MAKEINTRESOURCE(IDS_SOMECONTENT), 
    TDCBF_OK_BUTTON | TDCBF_CANCEL_BUTTON,
    TD_WARNING_ICON, 
    &nButtonPressed);

if (IDOK == nButtonPressed)
{
    // OK button pressed
}
else if (IDCANCEL == nButtonPressed)
{
    // Cancel pressed
}
```

## -see-also

<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>
