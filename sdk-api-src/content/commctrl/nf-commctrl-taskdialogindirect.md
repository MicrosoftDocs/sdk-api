---
UID: NF:commctrl.TaskDialogIndirect
title: TaskDialogIndirect function (commctrl.h)
description: The TaskDialogIndirect function creates, displays, and operates a task dialog.
helpviewer_keywords: ["TaskDialogIndirect","TaskDialogIndirect function [Windows Controls]","_shell_TaskDialogIndirect","_shell_TaskDialogIndirect_cpp","commctrl/TaskDialogIndirect","controls.TaskDialogIndirect","controls._shell_TaskDialogIndirect"]
old-location: controls\TaskDialogIndirect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\taskdialogs\taskdialogreference\taskdialogfunctions\taskdialogindirect.htm
ms.date: 12/05/2018
ms.keywords: TaskDialogIndirect, TaskDialogIndirect function [Windows Controls], _shell_TaskDialogIndirect, _shell_TaskDialogIndirect_cpp, commctrl/TaskDialogIndirect, controls.TaskDialogIndirect, controls._shell_TaskDialogIndirect
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
 - TaskDialogIndirect
 - commctrl/TaskDialogIndirect
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
 - TaskDialogIndirect
---

# TaskDialogIndirect function


## -description

The <b>TaskDialogIndirect</b> function creates, displays, and operates a task dialog. The task dialog contains application-defined icons, messages, title, verification check box, command links, push buttons, and radio buttons. This function can register a callback function to receive notification messages.

## -parameters

### -param pTaskConfig [in]

Type: <b>const <a href="/windows/desktop/api/commctrl/ns-commctrl-taskdialogconfig">TASKDIALOGCONFIG</a>*</b>

Pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-taskdialogconfig">TASKDIALOGCONFIG</a> structure that contains information used to display the task dialog.

### -param pnButton [out, optional]

Type: <b>int*</b>

Address of a variable that receives either:
				<ul>
<li>one of the button IDs specified in the <b>pButtons</b> member of the <i>pTaskConfig</i> parameter</li>
<li>one of the following values:</li>
</ul>


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
</table>
 

If this parameter is <b>NULL</b>, no value is returned.

### -param pnRadioButton [out, optional]

Type: <b>int*</b>

Address of a variable that receives one of the button IDs specified in the <b>pRadioButtons</b> member of the <i>pTaskConfig</i> parameter. If this parameter is <b>NULL</b>, no value is returned.

### -param pfVerificationFlagChecked [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Address of a variable that receives one of the following values.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The verification checkbox was checked when the dialog was dismissed.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The verification checkbox was not checked when the dialog was dismissed.</td>
</tr>
</table>
 

If this parameter is <b>NULL</b>, the verification checkbox is disabled.

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

When you use a task dialog box to indicate that the system is low on memory, the strings pointed to by the various string and icon members in the <a href="/windows/desktop/api/commctrl/ns-commctrl-taskdialogconfig">TASKDIALOGCONFIG</a> structure should not be taken from a resource file since an attempt to load the resource may fail.

 If you create a task dialog while a dialog box is present, use a handle to the dialog box as the <i>hWndParent</i> parameter. The <i>hWndParent</i> parameter should not identify a child window, such as a control in a dialog box. 

The parent window should not be hidden or disabled when this function is called. 


```

int nButtonPressed                  = 0;
TASKDIALOGCONFIG config             = {0};
const TASKDIALOG_BUTTON buttons[]   = { 
                                        { IDOK, L"Change password" }
                                      };
config.cbSize                       = sizeof(config);
config.hInstance                    = hInst;
config.dwCommonButtons              = TDCBF_CANCEL_BUTTON;
config.pszMainIcon                  = TD_WARNING_ICON;
config.pszMainInstruction           = L"Change Password";
config.pszContent                   = L"Remember your changed password.";
config.pButtons                     = buttons;
config.cButtons                     = ARRAYSIZE(buttons);

TaskDialogIndirect(&config, &nButtonPressed, NULL, NULL);
switch (nButtonPressed)
{
    case IDOK:
        break; // the user pressed button 0 (change password).
    case IDCANCEL:
        break; // user canceled the dialog
    default:
        break; // should never happen
}
```

## -see-also

<b></b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>