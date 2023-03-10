---
UID: NS:shlobj_core.DFMICS
title: DFMICS (shlobj_core.h)
description: Contains additional arguments used by DFM_INVOKECOMMANDEX.
helpviewer_keywords: ["*PDFMICS","CMIC_MASK_ASYNCOK","CMIC_MASK_CONTROL_DOWN","CMIC_MASK_FLAG_LOG_USAGE","CMIC_MASK_FLAG_NO_UI","CMIC_MASK_FLAG_SEP_VDM","CMIC_MASK_HOTKEY","CMIC_MASK_ICON","CMIC_MASK_NOASYNC","CMIC_MASK_NOZONECHECKS","CMIC_MASK_NO_CONSOLE","CMIC_MASK_PTINVOKE","CMIC_MASK_SHIFT_DOWN","CMIC_MASK_UNICODE","DFMICS","DFMICS structure [Windows Shell]","PDFMICS","PDFMICS structure pointer [Windows Shell]","_shell_DFMICS","shell.DFMICS","shlobj_core/DFMICS","shlobj_core/PDFMICS"]
old-location: shell\DFMICS.htm
tech.root: shell
ms.assetid: 2dbee891-6d5f-4ae1-8411-5d51cbab4457
ms.date: 12/05/2018
ms.keywords: '*PDFMICS, CMIC_MASK_ASYNCOK, CMIC_MASK_CONTROL_DOWN, CMIC_MASK_FLAG_LOG_USAGE, CMIC_MASK_FLAG_NO_UI, CMIC_MASK_FLAG_SEP_VDM, CMIC_MASK_HOTKEY, CMIC_MASK_ICON, CMIC_MASK_NOASYNC, CMIC_MASK_NOZONECHECKS, CMIC_MASK_NO_CONSOLE, CMIC_MASK_PTINVOKE, CMIC_MASK_SHIFT_DOWN, CMIC_MASK_UNICODE, DFMICS, DFMICS structure [Windows Shell], PDFMICS, PDFMICS structure pointer [Windows Shell], _shell_DFMICS, shell.DFMICS, shlobj_core/DFMICS, shlobj_core/PDFMICS'
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.typenames: DFMICS, *PDFMICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDFMICS
 - shlobj_core/PDFMICS
 - DFMICS
 - shlobj_core/DFMICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DFMICS
---

# DFMICS structure


## -description

Contains additional arguments used by <a href="/windows/desktop/shell/prophand-content-view">DFM_INVOKECOMMANDEX</a>.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.

### -field fMask

Type: <b>DWORD</b>

Zero, or one or more of the following flags that specify how to handle the data in the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> or <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a> structure pointed to by <b>pici</b>.



#### CMIC_MASK_HOTKEY

The <b>dwHotKey</b> member is valid.



#### CMIC_MASK_ICON

Not used.



#### CMIC_MASK_FLAG_NO_UI

The implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> is prevented from displaying user interface elements (for example, error messages) while carrying out a command.



#### CMIC_MASK_UNICODE

Used only when <b>pici</b> points to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a> structure. Indicates that the shortcut menu handler should use <b>lpVerbW</b>, <b>lpParametersW</b>, <b>lpTitleW</b>, and <b>lpDirectoryW</b> members instead of their ANSI equivalents. Because some shortcut menu handlers may not support Unicode, you should also pass valid ANSI strings in the <b>lpVerb</b>, <b>lpParameters</b>, <b>lpTitleW</b>, and <b>lpDirectory</b> members.



#### CMIC_MASK_NO_CONSOLE

If a shortcut menu handler needs to create a new process, it normally creates a new console. Setting the <b>CMIC_MASK_NO_CONSOLE</b> flag suppresses the creation of a new console.



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

Used only when <b>pici</b> points to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a> structure. The <b>ptInvoke</b> member is valid.

### -field lParam

Type: <b>LPARAM</b>

A pointer to a null-terminated string that contains additional arguments to the selected menu command. This member can be <b>NULL</b>.

### -field idCmdFirst

Type: <b>UINT</b>

The minimum value that the handler can specify for a menu item identifier.

### -field idDefMax

Type: <b>UINT</b>

The maximum value that the handler can specify for a menu item identifier.

### -field pici

Type: <b>LPCMINVOKECOMMANDINFO</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> or <b>CMINVOKECOMMANDINFO</b> structure.

### -field punkSite

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the site of the context menu handler.

