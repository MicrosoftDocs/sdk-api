---
UID: NF:shobjidl_core.IShellFolder.GetAttributesOf
title: IShellFolder::GetAttributesOf (shobjidl_core.h)
description: Gets the attributes of one or more file or folder objects contained in the object represented by IShellFolder.
helpviewer_keywords: ["GetAttributesOf","GetAttributesOf method [Windows Shell]","GetAttributesOf method [Windows Shell]","IShellFolder interface","GetAttributesOf method [Windows Shell]","IShellFolder2 interface","IShellFolder interface [Windows Shell]","GetAttributesOf method","IShellFolder.GetAttributesOf","IShellFolder2 interface [Windows Shell]","GetAttributesOf method","IShellFolder2::GetAttributesOf","IShellFolder::GetAttributesOf","_win32_IShellFolder_GetAttributesOf","shell.IShellFolder_GetAttributesOf","shobjidl_core/IShellFolder2::GetAttributesOf","shobjidl_core/IShellFolder::GetAttributesOf"]
old-location: shell\IShellFolder_GetAttributesOf.htm
tech.root: shell
ms.assetid: 3864b386-7653-4661-880c-e96c08ff0dbb
ms.date: 12/05/2018
ms.keywords: GetAttributesOf, GetAttributesOf method [Windows Shell], GetAttributesOf method [Windows Shell],IShellFolder interface, GetAttributesOf method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],GetAttributesOf method, IShellFolder.GetAttributesOf, IShellFolder2 interface [Windows Shell],GetAttributesOf method, IShellFolder2::GetAttributesOf, IShellFolder::GetAttributesOf, _win32_IShellFolder_GetAttributesOf, shell.IShellFolder_GetAttributesOf, shobjidl_core/IShellFolder2::GetAttributesOf, shobjidl_core/IShellFolder::GetAttributesOf
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
 - IShellFolder::GetAttributesOf
 - shobjidl_core/IShellFolder::GetAttributesOf
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
 - IShellFolder.GetAttributesOf
 - IShellFolder2.GetAttributesOf
---

# IShellFolder::GetAttributesOf


## -description

Gets the attributes of one or more file or folder objects contained in the object represented by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>.

## -parameters

### -param cidl [in]

Type: <b>UINT</b>

The number of items from which to retrieve attributes.

### -param apidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY*</b>

The address of an array of pointers to <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures, each of which uniquely identifies an item relative to the parent folder. Each <b>ITEMIDLIST</b> structure must contain exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure followed by a terminating zero.

### -param rgfInOut [in, out]

Type: <b>SFGAOF*</b>

Pointer to a single <b>ULONG</b> value that, on entry, contains the bitwise <a href="/windows/desktop/shell/sfgao">SFGAO</a> attributes that the calling application is requesting. On exit, this value contains the requested attributes that are common to all of the specified items.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To optimize this operation, do not return unspecified flags.

For a folder object, the <a href="/windows/desktop/shell/sfgao">SFGAO_BROWSABLE</a> attribute implies that the client can bind to this object as shown in a general form here.


```cpp
IShellFolder::BindToObject(..., pidl, IID_IShellFolder, &psfItem);

```


The client can then create an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> on that item through this statement.


```cpp
psfItem->CreateViewObject(..., IID_IShellView,...);

```


The <a href="/windows/desktop/shell/sfgao">SFGAO_DROPTARGET</a> attribute implies that the client can bind to an instance of <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> for this folder by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> as shown here.

                


```cpp
IShellFolder::GetUIObjectOf(hwnd, 1, &pidl, IID_IDropTarget, NULL, &pv)

```


The SFGAO_NONENUMERATED attribute indicates an item that is not returned by the enumerator created by the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>