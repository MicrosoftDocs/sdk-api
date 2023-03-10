---
UID: NF:shobjidl_core.IShellMenu.GetShellFolder
title: IShellMenu::GetShellFolder (shobjidl_core.h)
description: Gets the folder that the menu band is set to browse.
helpviewer_keywords: ["GetShellFolder","GetShellFolder method [Windows Shell]","GetShellFolder method [Windows Shell]","IShellMenu interface","IShellMenu interface [Windows Shell]","GetShellFolder method","IShellMenu.GetShellFolder","IShellMenu::GetShellFolder","SMINIT_CACHED","SMINIT_DEFAULT","SMINIT_HORIZONTAL","SMINIT_RESTRICT_DRAGDROP","SMINIT_TOPLEVEL","SMINIT_VERTICAL","_shell_IShellMenu_GetShellFolder","shell.IShellMenu_GetShellFolder","shobjidl_core/IShellMenu::GetShellFolder"]
old-location: shell\IShellMenu_GetShellFolder.htm
tech.root: shell
ms.assetid: 6f88e1ee-950f-41b8-ad53-3bd7e8772f42
ms.date: 12/05/2018
ms.keywords: GetShellFolder, GetShellFolder method [Windows Shell], GetShellFolder method [Windows Shell],IShellMenu interface, IShellMenu interface [Windows Shell],GetShellFolder method, IShellMenu.GetShellFolder, IShellMenu::GetShellFolder, SMINIT_CACHED, SMINIT_DEFAULT, SMINIT_HORIZONTAL, SMINIT_RESTRICT_DRAGDROP, SMINIT_TOPLEVEL, SMINIT_VERTICAL, _shell_IShellMenu_GetShellFolder, shell.IShellMenu_GetShellFolder, shobjidl_core/IShellMenu::GetShellFolder
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellMenu::GetShellFolder
 - shobjidl_core/IShellMenu::GetShellFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellMenu.GetShellFolder
---

# IShellMenu::GetShellFolder


## -description

Gets the folder that the menu band is set to browse.

## -parameters

### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns successfully, contains a pointer to a set of flag values that specify how the menu band operates.


Can return any of the following flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMINIT_DEFAULT"></a><a id="sminit_default"></a><dl>
<dt><b>SMINIT_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
No options.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_RESTRICT_DRAGDROP"></a><a id="sminit_restrict_dragdrop"></a><dl>
<dt><b>SMINIT_RESTRICT_DRAGDROP</b></dt>
</dl>
</td>
<td width="60%">
Do not allow drag-and-drop.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_TOPLEVEL"></a><a id="sminit_toplevel"></a><dl>
<dt><b>SMINIT_TOPLEVEL</b></dt>
</dl>
</td>
<td width="60%">
This is the top band.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_CACHED"></a><a id="sminit_cached"></a><dl>
<dt><b>SMINIT_CACHED</b></dt>
</dl>
</td>
<td width="60%">
Do not destroy the band when the window is closed.

</td>
</tr>
</table>
 


Always returns one of the following flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMINIT_VERTICAL"></a><a id="sminit_vertical"></a><dl>
<dt><b>SMINIT_VERTICAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies a vertical band.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_HORIZONTAL"></a><a id="sminit_horizontal"></a><dl>
<dt><b>SMINIT_HORIZONTAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies a horizontal band.

</td>
</tr>
</table>

### -param ppidl [out]

Type: <b>PCIDLIST_ABSOLUTE*</b>

When this method returns, contains the address of the folder's fully qualified <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

### -param riid [in]

Type: <b>REFIID</b>

The REFIID for the target folder.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the address of a pointer to the Shell folder object referenced by the <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.