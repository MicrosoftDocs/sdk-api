---
UID: NS:shobjidl_core._CMINVOKECOMMANDINFOEX
title: CMINVOKECOMMANDINFOEX (shobjidl_core.h)
description: Contains extended information about a shortcut menu command. This structure is an extended version of CMINVOKECOMMANDINFO that allows the use of Unicode values.
helpviewer_keywords: ["*LPCMINVOKECOMMANDINFOEX","CMIC_MASK_ASYNCOK","CMIC_MASK_CONTROL_DOWN","CMIC_MASK_FLAG_LOG_USAGE","CMIC_MASK_FLAG_NO_UI","CMIC_MASK_FLAG_SEP_VDM","CMIC_MASK_HASLINKNAME","CMIC_MASK_HASTITLE","CMIC_MASK_HOTKEY","CMIC_MASK_ICON","CMIC_MASK_NOASYNC","CMIC_MASK_NOZONECHECKS","CMIC_MASK_NO_CONSOLE","CMIC_MASK_PTINVOKE","CMIC_MASK_SHIFT_DOWN","CMIC_MASK_UNICODE","CMINVOKECOMMANDINFOEX","CMINVOKECOMMANDINFOEX structure [Windows Shell]","LPCMINVOKECOMMANDINFOEX","LPCMINVOKECOMMANDINFOEX structure pointer [Windows Shell]","_CMINVOKECOMMANDINFOEX","_win32_CmInvokeCommandInfoEx","shell.CmInvokeCommandInfoEx","shobjidl_core/CMINVOKECOMMANDINFOEX","shobjidl_core/LPCMINVOKECOMMANDINFOEX"]
old-location: shell\CmInvokeCommandInfoEx.htm
tech.root: shell
ms.assetid: c4c7f053-fdb1-4bba-9eb9-a514ce1d90f6
ms.date: 12/05/2018
ms.keywords: '*LPCMINVOKECOMMANDINFOEX, CMIC_MASK_ASYNCOK, CMIC_MASK_CONTROL_DOWN, CMIC_MASK_FLAG_LOG_USAGE, CMIC_MASK_FLAG_NO_UI, CMIC_MASK_FLAG_SEP_VDM, CMIC_MASK_HASLINKNAME, CMIC_MASK_HASTITLE, CMIC_MASK_HOTKEY, CMIC_MASK_ICON, CMIC_MASK_NOASYNC, CMIC_MASK_NOZONECHECKS, CMIC_MASK_NO_CONSOLE, CMIC_MASK_PTINVOKE, CMIC_MASK_SHIFT_DOWN, CMIC_MASK_UNICODE, CMINVOKECOMMANDINFOEX, CMINVOKECOMMANDINFOEX structure [Windows Shell], LPCMINVOKECOMMANDINFOEX, LPCMINVOKECOMMANDINFOEX structure pointer [Windows Shell], _CMINVOKECOMMANDINFOEX, _win32_CmInvokeCommandInfoEx, shell.CmInvokeCommandInfoEx, shobjidl_core/CMINVOKECOMMANDINFOEX, shobjidl_core/LPCMINVOKECOMMANDINFOEX'
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: CMINVOKECOMMANDINFOEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMINVOKECOMMANDINFOEX
 - shobjidl_core/_CMINVOKECOMMANDINFOEX
 - CMINVOKECOMMANDINFOEX
 - shobjidl_core/CMINVOKECOMMANDINFOEX
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
 - CMINVOKECOMMANDINFOEX
---

# CMINVOKECOMMANDINFOEX structure


## -description

Contains extended information about a shortcut menu command. This structure is an extended version of <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> that allows the use of Unicode values.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes. This member should be filled in by callers of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> and tested by the implementations to know that the structure is a <b>CMINVOKECOMMANDINFOEX</b> structure rather than <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a>.

### -field fMask

Type: <b>DWORD</b>

Zero, or one or more of the following flags are set to indicate desired behavior and indicate that other fields in the structure are to be used.



#### CMIC_MASK_HOTKEY

The <b>dwHotKey</b> member is valid.



#### CMIC_MASK_ICON

The <b>hIcon</b> member is valid. As of Windows Vista this flag is not used.



#### CMIC_MASK_FLAG_NO_UI

The implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> is prevented from displaying user interface elements (for example, error messages) while carrying out a command.



#### CMIC_MASK_UNICODE

The shortcut menu handler should use <b>lpVerbW</b>, <b>lpParametersW</b>, <b>lpDirectoryW</b>, and <b>lpTitleW</b> members instead of their ANSI equivalents. Because some shortcut menu handlers may not support Unicode, you should also pass valid ANSI strings in the <b>lpVerb</b>, <b>lpParameters</b>, <b>lpDirectory</b>, and <b>lpTitle</b> members.



#### CMIC_MASK_NO_CONSOLE

If a shortcut menu handler needs to create a new process, it will normally create a new console. Setting the <b>CMIC_MASK_NO_CONSOLE</b> flag suppresses the creation of a new console.



#### CMIC_MASK_HASLINKNAME

The <b>lpTitle</b> member contains a full path to a shortcut file.  Use in conjunction with <b>CMIC_MASK_HASTITLE</b>.
        
                                

<div class="alert"><b>Note</b>  This value is not supported in Windows Vista and later systems.</div>
<div> </div>


#### CMIC_MASK_HASTITLE

The <b>lpTitle</b> member is valid.
        
                                

<div class="alert"><b>Note</b>  This value is not supported in Windows Vista and later systems.</div>
<div> </div>


#### CMIC_MASK_FLAG_SEP_VDM

This flag is valid only when referring to a 16-bit Windows-based application. If set, the application that the shortcut points to runs in a private Virtual DOS Machine (VDM). See Remarks.



#### CMIC_MASK_ASYNCOK

The implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> can spin off a new thread or process to handle the call and does not need to block on completion of the function being invoked. For example, if the verb is "delete" the <b>IContextMenu::InvokeCommand</b> call may return before all of the items have been deleted. Since this is advisory, calling applications that specify this flag cannot guarantee that this request will be honored if they are not familiar with the implementation of the verb that they are invoking.



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



#### CMIC_MASK_PTINVOKE

The <b>ptInvoke</b> member is valid.

### -field hwnd

Type: <b>HWND</b>

A handle to the window that is the owner of the shortcut menu. An extension can also use this handle as the owner of any message boxes or dialog boxes it displays. Callers must specify a legitimate HWND that can be used as the owner window for any UI that may be displayed. Failing to specify an HWND when calling from a UI thread (one with windows already created) will result in reentrancy and possible bugs in the implementation of a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> call.

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

Optional parameters. This member is always <b>NULL</b> for menu items inserted by a Shell extension.

### -field lpDirectory

Type: <b>LPCSTR</b>

An optional working directory name. This member is always <b>NULL</b> for menu items inserted by a Shell extension.

### -field nShow

Type: <b>int</b>

A set of SW_ values to pass to the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function if the command displays a window or starts an application.

### -field dwHotKey

Type: <b>DWORD</b>

An optional keyboard shortcut to assign to any application activated by the command. If the 
    					<b>fMask</b> member does not specify <b>CMIC_MASK_HOTKEY</b>, this member is ignored.

### -field hIcon

Type: <b>HANDLE</b>

An icon to use for any application activated by the command. If the <b>fMask</b> member does not specify <b>CMIC_MASK_ICON</b>, this member is ignored.

### -field lpTitle

Type: <b>LPCSTR</b>

An ASCII title.

### -field lpVerbW

Type: <b>LPCWSTR</b>

A Unicode verb, for those commands that can use it.

### -field lpParametersW

Type: <b>LPCWSTR</b>

A Unicode parameters, for those commands that can use it.

### -field lpDirectoryW

Type: <b>LPCWSTR</b>

A Unicode directory, for those commands that can use it.

### -field lpTitleW

Type: <b>LPCWSTR</b>

A Unicode title.

### -field ptInvoke

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The point where the command is invoked. If the <b>fMask</b> member does not specify <b>CMIC_MASK_PTINVOKE</b>, this member is ignored. This member is not valid prior to Internet Explorer 4.0.

## -remarks

Although the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> declaration specifies a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> structure for the <i>pici</i> parameter, it can also accept a <b>CMINVOKECOMMANDINFOEX</b> structure. If you are implementing this method, you must inspect <b>cbSize</b> to determine which structure has been passed. 
			

By default, all 16-bit Windows-based applications run as threads in a single, shared VDM. The advantage of running separately is that a crash only terminates the single VDM; any other programs running in distinct VDMs continue to function normally. Also, 16-bit Windows-based applications that are run in separate VDMs have separate input queues. That means that if one application stops responding momentarily, applications in separate VDMs continue to receive input. The disadvantage of running separately is that it takes significantly more memory to do so.

<b>CMINVOKECOMMANDINFOEX</b> itself is defined in Shobjidl.h, but you must also include Shellapi.h to have full access to all flags.

<div class="alert"><b>Note</b>  Prior to Windows Vista, this structure was declared in Shlobj.h.</div>
<div> </div>