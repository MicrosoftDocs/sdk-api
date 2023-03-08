---
UID: NF:shobjidl_core.IShellFolder.GetUIObjectOf
title: IShellFolder::GetUIObjectOf (shobjidl_core.h)
description: Gets an object that can be used to carry out actions on the specified file objects or folders.
helpviewer_keywords: ["GetUIObjectOf","GetUIObjectOf method [Windows Shell]","GetUIObjectOf method [Windows Shell]","IShellFolder interface","GetUIObjectOf method [Windows Shell]","IShellFolder2 interface","IShellFolder interface [Windows Shell]","GetUIObjectOf method","IShellFolder.GetUIObjectOf","IShellFolder2 interface [Windows Shell]","GetUIObjectOf method","IShellFolder2::GetUIObjectOf","IShellFolder::GetUIObjectOf","_win32_IShellFolder_GetUIObjectOf","shell.IShellFolder_GetUIObjectOf","shobjidl_core/IShellFolder2::GetUIObjectOf","shobjidl_core/IShellFolder::GetUIObjectOf"]
old-location: shell\IShellFolder_GetUIObjectOf.htm
tech.root: shell
ms.assetid: ec863dbf-8ec9-4952-8912-575125e6dd09
ms.date: 12/05/2018
ms.keywords: GetUIObjectOf, GetUIObjectOf method [Windows Shell], GetUIObjectOf method [Windows Shell],IShellFolder interface, GetUIObjectOf method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],GetUIObjectOf method, IShellFolder.GetUIObjectOf, IShellFolder2 interface [Windows Shell],GetUIObjectOf method, IShellFolder2::GetUIObjectOf, IShellFolder::GetUIObjectOf, _win32_IShellFolder_GetUIObjectOf, shell.IShellFolder_GetUIObjectOf, shobjidl_core/IShellFolder2::GetUIObjectOf, shobjidl_core/IShellFolder::GetUIObjectOf
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder::GetUIObjectOf
 - shobjidl_core/IShellFolder::GetUIObjectOf
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
 - IShellFolder.GetUIObjectOf
 - IShellFolder2.GetUIObjectOf
---

# IShellFolder::GetUIObjectOf


## -description

Gets an object that can be used to carry out actions on the specified file objects or folders.

## -parameters

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the owner window that the client should specify if it displays a dialog box or message box.

### -param cidl [in]

Type: <b>UINT</b>

The number of file objects or subfolders specified in the <i>apidl</i> parameter.

### -param apidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY</b>

The address of an array of pointers to <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures, each of which uniquely identifies a file object or subfolder relative to the parent folder. Each item identifier list must contain exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure followed by a terminating zero.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>. This can be any valid interface identifier that can be created for an item. The most common identifiers used by the Shell are listed in the comments at the end of this reference.

### -param rgfReserved [in, out]

Type: <b>UINT*</b>

Reserved.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>cidl</i> is greater than one, the <b>IShellFolder::GetUIObjectOf</b> implementation should only succeed if it can create one object for all items specified in <i>apidl</i>. If the implementation cannot create one object for all items, this method will fail.

The following are the most common interface identifiers the Shell uses when requesting an interface from this method. The list also indicates if <i>cidl</i> can be greater than one for the requested interface.

<table class="clsStd">
<tr>
<th>Interface Identifier</th>
<th>Allowed <i>cidl</i> Value</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a>
</td>
<td>The <i>cidl</i> parameter can be greater than or equal to one.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a>
</td>
<td>The <i>cidl</i> parameter can be greater than or equal to one.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>
</td>
<td>The <i>cidl</i> parameter can be greater than or equal to one.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>
</td>
<td>The <i>cidl</i> parameter can only be one.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a>
</td>
<td>The <i>cidl</i> parameter can only be one.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo">IQueryInfo</a>
</td>
<td>The <i>cidl</i> parameter can only be one.</td>
</tr>
</table>
 

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>