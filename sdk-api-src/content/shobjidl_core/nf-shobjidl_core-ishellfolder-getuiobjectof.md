---
UID: NF:shobjidl_core.IShellFolder.GetUIObjectOf
title: IShellFolder::GetUIObjectOf (shobjidl_core.h)
author: windows-sdk-content
description: Gets an object that can be used to carry out actions on the specified file objects or folders.
old-location: shell\IShellFolder_GetUIObjectOf.htm
tech.root: shell
ms.assetid: ec863dbf-8ec9-4952-8912-575125e6dd09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUIObjectOf, GetUIObjectOf method [Windows Shell], GetUIObjectOf method [Windows Shell],IShellFolder interface, GetUIObjectOf method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],GetUIObjectOf method, IShellFolder.GetUIObjectOf, IShellFolder2 interface [Windows Shell],GetUIObjectOf method, IShellFolder2::GetUIObjectOf, IShellFolder::GetUIObjectOf, _win32_IShellFolder_GetUIObjectOf, shell.IShellFolder_GetUIObjectOf, shobjidl_core/IShellFolder2::GetUIObjectOf, shobjidl_core/IShellFolder::GetUIObjectOf
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The address of an array of pointers to <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures, each of which uniquely identifies a file object or subfolder relative to the parent folder. Each item identifier list must contain exactly one <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure followed by a terminating zero.


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




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
<a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>
</td>
<td>The <i>cidl</i> parameter can be greater than or equal to one.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a>
</td>
<td>The <i>cidl</i> parameter can be greater than or equal to one.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>
</td>
<td>The <i>cidl</i> parameter can be greater than or equal to one.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>
</td>
<td>The <i>cidl</i> parameter can only be one.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f8e0ab98-c225-4cc1-93f8-b7ab6b2f706f">IExtractIcon</a>
</td>
<td>The <i>cidl</i> parameter can only be one.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7e256ed3-b3c7-4f9d-b3a0-e33c46fa2573">IQueryInfo</a>
</td>
<td>The <i>cidl</i> parameter can only be one.</td>
</tr>
</table>
 

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a>
 

 

