---
UID: NF:shlobj_core.SHShellFolderView_Message
title: SHShellFolderView_Message function (shlobj_core.h)
description: SHShellFolderView_Message may be altered or unavailable.
helpviewer_keywords: ["SHShellFolderView_Message","SHShellFolderView_Message function [Windows Shell]","_win32_SHShellFolderView_Message","shell.SHShellFolderView_Message","shlobj_core/SHShellFolderView_Message"]
old-location: shell\SHShellFolderView_Message.htm
tech.root: shell
ms.assetid: f5722a4f-d830-4c31-9275-13e800408681
ms.date: 12/05/2018
ms.keywords: SHShellFolderView_Message, SHShellFolderView_Message function [Windows Shell], _win32_SHShellFolderView_Message, shell.SHShellFolderView_Message, shlobj_core/SHShellFolderView_Message
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHShellFolderView_Message
 - shlobj_core/SHShellFolderView_Message
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHShellFolderView_Message
---

# SHShellFolderView_Message function


## -description

<p class="CCE_Message">[<b>SHShellFolderView_Message</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sends a message to the shell's default <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a> implementation (DefView).

## -parameters

### -param hwndMain [in]

Type: <b>HWND</b>

A handle to the window that receives the message.

### -param uMsg

Type: <b>UINT</b>

The message to send. The following is a list of possible messages.

						

<table class="clsStd">
<tr>
<th>Message</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/samples-usingimagefactory">SFVM_ADDOBJECT</a>
</td>
<td>Adds an object to the shell view.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getselectedobjects">SFVM_GETSELECTEDOBJECTS</a>
</td>
<td>Retrieves an array of PIDLs for all selected objects.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-rearrange">SFVM_REARRANGE</a>
</td>
<td>Notifies the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> to rearrange its items.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-removeobject">SFVM_REMOVEOBJECT</a>
</td>
<td>Removes an object from the shell view.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-setclipboard">SFVM_SETCLIPBOARD</a>
</td>
<td>Notifies the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> when one of its objects is placed on the clipboard as a result of a menu command.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-setitempos">SFVM_SETITEMPOS</a>
</td>
<td>Sets the position of an item in the shell view.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-setpoints">SFVM_SETPOINTS</a>
</td>
<td>Sets the points of the currently selected objects to the data object on <b>copy</b> and <b>cut</b> commands.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-updateobject">SFVM_UPDATEOBJECT</a>
</td>
<td>Updates an object by passing a pointer to an array of two PIDLs.</td>
</tr>
</table>

### -param lParam

Type: <b>LPARAM</b>

Contents of this value depend on the message passed in <i>uMsg</i>. See individual message topics for more information.

## -returns

Type: <b>LRESULT</b>

The return value depends on the message passed in <i>uMsg</i>. See individual message topics for more information.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a>