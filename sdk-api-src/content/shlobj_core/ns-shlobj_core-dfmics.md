---
UID: NS:shlobj_core.DFMICS
title: DFMICS
author: windows-sdk-content
description: Contains additional arguments used by DFM_INVOKECOMMANDEX.
old-location: shell\DFMICS.htm
old-project: shell
ms.assetid: 2dbee891-6d5f-4ae1-8411-5d51cbab4457
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: "*PDFMICS, CMIC_MASK_ASYNCOK, CMIC_MASK_CONTROL_DOWN, CMIC_MASK_FLAG_LOG_USAGE, CMIC_MASK_FLAG_NO_UI, CMIC_MASK_FLAG_SEP_VDM, CMIC_MASK_HOTKEY, CMIC_MASK_ICON, CMIC_MASK_NOASYNC, CMIC_MASK_NOZONECHECKS, CMIC_MASK_NO_CONSOLE, CMIC_MASK_PTINVOKE, CMIC_MASK_SHIFT_DOWN, CMIC_MASK_UNICODE, DFMICS, DFMICS structure [Windows Shell], PDFMICS, PDFMICS structure pointer [Windows Shell], _shell_DFMICS, shell.DFMICS, shlobj_core/DFMICS, shlobj_core/PDFMICS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DFMICS, *PDFMICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DFMICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# DFMICS structure


## -description


Contains additional arguments used by <a href="https://msdn.microsoft.com/6ef885e5-2ddd-4a1b-9f8e-016a74e292b1">DFM_INVOKECOMMANDEX</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field fMask

Type: <b>DWORD</b>

Zero, or one or more of the following flags that specify how to handle the data in the <a href="https://msdn.microsoft.com/1da79d98-5a2f-4c43-aab2-8ae7c3b345b2">CMINVOKECOMMANDINFO</a> or <a href="https://msdn.microsoft.com/c4c7f053-fdb1-4bba-9eb9-a514ce1d90f6">CMINVOKECOMMANDINFOEX</a> structure pointed to by <b>pici</b>.



#### CMIC_MASK_HOTKEY

The <b>dwHotKey</b> member is valid.



#### CMIC_MASK_ICON

Not used.



#### CMIC_MASK_FLAG_NO_UI

The implementation of <a href="https://msdn.microsoft.com/f3aaa84c-3b33-4288-a46a-cd80d3fa89cf">IContextMenu::InvokeCommand</a> is prevented from displaying user interface elements (for example, error messages) while carrying out a command.



#### CMIC_MASK_UNICODE

Used only when <b>pici</b> points to a <a href="https://msdn.microsoft.com/c4c7f053-fdb1-4bba-9eb9-a514ce1d90f6">CMINVOKECOMMANDINFOEX</a> structure. Indicates that the shortcut menu handler should use <b>lpVerbW</b>, <b>lpParametersW</b>, <b>lpTitleW</b>, and <b>lpDirectoryW</b> members instead of their ANSI equivalents. Because some shortcut menu handlers may not support Unicode, you should also pass valid ANSI strings in the <b>lpVerb</b>, <b>lpParameters</b>, <b>lpTitleW</b>, and <b>lpDirectory</b> members.



#### CMIC_MASK_NO_CONSOLE

If a shortcut menu handler needs to create a new process, it normally creates a new console. Setting the <b>CMIC_MASK_NO_CONSOLE</b> flag suppresses the creation of a new console.



#### CMIC_MASK_FLAG_SEP_VDM

This flag is valid only when referring to a 16-bit Windows-based application. If set, the application that the shortcut points to runs in a private Virtual DOS Machine (VDM). See Remarks.



#### CMIC_MASK_ASYNCOK

The implementation of <a href="https://msdn.microsoft.com/f3aaa84c-3b33-4288-a46a-cd80d3fa89cf">IContextMenu::InvokeCommand</a> can spin off a new thread or process to handle the call and does not need to block on completion of the function being invoked. For example, if the verb is "delete" the <b>IContextMenu::InvokeCommand</b> call may return before all of the items have been deleted. Since this is advisory, calling applications that specify this flag cannot guarantee that this request will be honored if they are not familiar with the implementation of the verb that they are invoking.



#### CMIC_MASK_NOASYNC

<b>Windows Vista and later.</b> The implementation of <a href="https://msdn.microsoft.com/f3aaa84c-3b33-4288-a46a-cd80d3fa89cf">IContextMenu::InvokeCommand</a> should be synchronous, not returning before it is complete. Since this is recommended, calling applications that specify this flag cannot guarantee that this request will be honored if they are not familiar with the implementation of the verb that they are invoking.



#### CMIC_MASK_SHIFT_DOWN

The SHIFT key is pressed.  Use this instead of polling the current state of the keyboard that may have changed since the verb was invoked.



#### CMIC_MASK_CONTROL_DOWN

The CTRL key is pressed. Use this instead of polling the current state of the keyboard that may have changed since the verb was invoked.



#### CMIC_MASK_FLAG_LOG_USAGE

Indicates that the implementation of <a href="https://msdn.microsoft.com/f3aaa84c-3b33-4288-a46a-cd80d3fa89cf">IContextMenu::InvokeCommand</a> might want to keep track of the item being invoked for features like the "Recent documents" menu.




#### CMIC_MASK_NOZONECHECKS

Do not perform a zone check. This flag allows <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> to bypass zone checking put into place by <a href="https://msdn.microsoft.com/2ebc3197-aa28-446e-8452-8ff71764fa9d">IAttachmentExecute</a>.



#### CMIC_MASK_PTINVOKE

Used only when <b>pici</b> points to a <a href="https://msdn.microsoft.com/c4c7f053-fdb1-4bba-9eb9-a514ce1d90f6">CMINVOKECOMMANDINFOEX</a> structure. The <b>ptInvoke</b> member is valid.


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

A pointer to a <a href="https://msdn.microsoft.com/1da79d98-5a2f-4c43-aab2-8ae7c3b345b2">CMINVOKECOMMANDINFO</a> or <b>CMINVOKECOMMANDINFO</b> structure.


### -field punkSite

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the site of the context menu handler.

