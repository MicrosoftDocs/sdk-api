---
UID: NS:shobjidl_core._CMINVOKECOMMANDINFO
title: CMINVOKECOMMANDINFO (shobjidl_core.h)
description: Contains information needed by IContextMenu::InvokeCommand to invoke a shortcut menu command.
helpviewer_keywords: ["*LPCMINVOKECOMMANDINFO","CMIC_MASK_ASYNCOK","CMIC_MASK_CONTROL_DOWN","CMIC_MASK_FLAG_LOG_USAGE","CMIC_MASK_FLAG_NO_UI","CMIC_MASK_FLAG_SEP_VDM","CMIC_MASK_HOTKEY","CMIC_MASK_ICON","CMIC_MASK_NOASYNC","CMIC_MASK_NOZONECHECKS","CMIC_MASK_NO_CONSOLE","CMIC_MASK_SHIFT_DOWN","CMINVOKECOMMANDINFO","CMINVOKECOMMANDINFO structure [Windows Shell]","PCCMINVOKECOMMANDINFO","PCCMINVOKECOMMANDINFO structure pointer [Windows Shell]","_CMINVOKECOMMANDINFO","_win32_CMINVOKECOMMANDINFO","shell.CMINVOKECOMMANDINFO","shobjidl_core/CMINVOKECOMMANDINFO","shobjidl_core/PCCMINVOKECOMMANDINFO"]
old-location: shell\CMINVOKECOMMANDINFO.htm
tech.root: shell
ms.assetid: 1da79d98-5a2f-4c43-aab2-8ae7c3b345b2
ms.date: 12/05/2018
ms.keywords: '*LPCMINVOKECOMMANDINFO, CMIC_MASK_ASYNCOK, CMIC_MASK_CONTROL_DOWN, CMIC_MASK_FLAG_LOG_USAGE, CMIC_MASK_FLAG_NO_UI, CMIC_MASK_FLAG_SEP_VDM, CMIC_MASK_HOTKEY, CMIC_MASK_ICON, CMIC_MASK_NOASYNC, CMIC_MASK_NOZONECHECKS, CMIC_MASK_NO_CONSOLE, CMIC_MASK_SHIFT_DOWN, CMINVOKECOMMANDINFO, CMINVOKECOMMANDINFO structure [Windows Shell], PCCMINVOKECOMMANDINFO, PCCMINVOKECOMMANDINFO structure pointer [Windows Shell], _CMINVOKECOMMANDINFO, _win32_CMINVOKECOMMANDINFO, shell.CMINVOKECOMMANDINFO, shobjidl_core/CMINVOKECOMMANDINFO, shobjidl_core/PCCMINVOKECOMMANDINFO'
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CMINVOKECOMMANDINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMINVOKECOMMANDINFO
 - shobjidl_core/_CMINVOKECOMMANDINFO
 - CMINVOKECOMMANDINFO
 - shobjidl_core/CMINVOKECOMMANDINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - CMINVOKECOMMANDINFO
---

# CMINVOKECOMMANDINFO structure


## -description

Contains information needed by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> to invoke a shortcut menu command.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.

### -field fMask

Type: <b>DWORD</b>

Zero, or one or more of the following flags.



#### CMIC_MASK_HOTKEY

The <b>dwHotKey</b> member is valid.



#### CMIC_MASK_ICON

The <b>hIcon</b> member is valid. As of Windows Vista this flag is not used.



#### CMIC_MASK_FLAG_NO_UI

The system is prevented from displaying user interface elements (for example, error messages) while carrying out a command.



#### CMIC_MASK_NO_CONSOLE

If a shortcut menu handler needs to create a new process, it will normally create a new console. Setting the <b>CMIC_MASK_NO_CONSOLE</b> flag suppresses the creation of a new console.



#### CMIC_MASK_FLAG_SEP_VDM

This flag is valid only when referring to a 16-bit Windows-based application. If set, the application that the shortcut points to runs in a private Virtual DOS Machine (VDM). See Remarks.



#### CMIC_MASK_ASYNCOK

Wait for the DDE conversation to terminate before returning.



#### CMIC_MASK_NOASYNC

<b>Windows Vista and later.</b> The implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> should be synchronous, not returning before it is complete. Since this is recommended, calling applications that specify this flag cannot guarantee that this request will be honored if they are not familiar with the implementation of the verb that they are invoking.



#### CMIC_MASK_SHIFT_DOWN

The SHIFT key is pressed.  Use this instead of polling the current state of the keyboard that may have changed since the verb was invoked.



#### CMIC_MASK_CONTROL_DOWN

The CTRL key is pressed. Use this instead of polling the current state of the keyboard that may have changed since the verb was invoked.



#### CMIC_MASK_FLAG_LOG_USAGE

Indicates that the implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> might want to keep track of the item being invoked for features like the "Recent documents" menu.



#### CMIC_MASK_NOZONECHECKS

Do not perform a zone check. This flag allows <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> to bypass zone checking put into place by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute">IAttachmentExecute</a>.

### -field hwnd

Type: <b>HWND</b>

A handle to the window that is the owner of the shortcut menu. An extension can also use this handle as the owner of any message boxes or dialog boxes it displays.

### -field lpVerb

Type: <b>LPCSTR</b>

The address of a null-terminated string that specifies the language-independent name of the command to carry out. This member is typically a string when a command is being activated by an application. The system provides predefined constant values for the following command strings.

<table class="clsStd">
<tr>
<th>Constant</th>
<th>Command string</th>
</tr>
<tr>
<td>CMDSTR_RUNAS</td>
<td>"RunAs"</td>
</tr>
<tr>
<td>CMDSTR_PRINT</td>
<td>"Print"</td>
</tr>
<tr>
<td>CMDSTR_PREVIEW</td>
<td>"Preview"</td>
</tr>
<tr>
<td>CMDSTR_OPEN</td>
<td>"Open"</td>
</tr>
</table>
 

This is not a fixed set; new canonical verbs can be invented by context menu handlers and applications can invoke them.

If a canonical verb exists and a menu handler does not implement the canonical verb, it must return a failure code to enable the next handler to be able to handle this verb. Failing to do this will break functionality in the system including <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>.

Alternatively, rather than a pointer, this parameter can be <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(offset) where <i>offset</i> is the menu-identifier offset of the command to carry out. Implementations can use the <a href="/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a> macro to detect that this alternative is being employed. The Shell uses this alternative when the user chooses a menu command.

### -field lpParameters

Type: <b>LPCSTR</b>

An optional string containing parameters that are passed to the command. The format of this string is determined by the command that is to be invoked. This member is always <b>NULL</b> for menu items inserted by a Shell extension.

### -field lpDirectory

Type: <b>LPCSTR</b>

An optional working directory name. This member is always <b>NULL</b> for menu items inserted by a Shell extension.

### -field nShow

Type: <b>int</b>

A set of SW_ values to pass to the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function if the command displays a window or starts an application.

### -field dwHotKey

Type: <b>DWORD</b>

An optional keyboard shortcut to assign to any application activated by the command. If the <b>fMask</b> parameter does not specify <b>CMIC_MASK_HOTKEY</b>, this member is ignored.

### -field hIcon

Type: <b>HANDLE</b>

An icon to use for any application activated by the command. If the <b>fMask</b> member does not specify <b>CMIC_MASK_ICON</b>, this member is ignored.

## -remarks

Although the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> declaration specifies a <b>CMINVOKECOMMANDINFO</b> structure for the <i>pici</i> parameter, it can also accept a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a> structure. If you are implementing this method, you must inspect <b>cbSize</b> to determine which structure has been passed.