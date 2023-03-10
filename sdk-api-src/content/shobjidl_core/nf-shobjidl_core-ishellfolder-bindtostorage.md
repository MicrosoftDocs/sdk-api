---
UID: NF:shobjidl_core.IShellFolder.BindToStorage
title: IShellFolder::BindToStorage (shobjidl_core.h)
description: Requests a pointer to an object's storage interface.
helpviewer_keywords: ["BindToStorage","BindToStorage method [Windows Shell]","BindToStorage method [Windows Shell]","IShellFolder interface","BindToStorage method [Windows Shell]","IShellFolder2 interface","IShellFolder interface [Windows Shell]","BindToStorage method","IShellFolder.BindToStorage","IShellFolder2 interface [Windows Shell]","BindToStorage method","IShellFolder2::BindToStorage","IShellFolder::BindToStorage","_win32_IShellFolder_BindToStorage","shell.IShellFolder_BindToStorage","shobjidl_core/IShellFolder2::BindToStorage","shobjidl_core/IShellFolder::BindToStorage"]
old-location: shell\IShellFolder_BindToStorage.htm
tech.root: shell
ms.assetid: 6abd12bb-5c85-4f3b-a6ad-a7c05ce02ce3
ms.date: 12/05/2018
ms.keywords: BindToStorage, BindToStorage method [Windows Shell], BindToStorage method [Windows Shell],IShellFolder interface, BindToStorage method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],BindToStorage method, IShellFolder.BindToStorage, IShellFolder2 interface [Windows Shell],BindToStorage method, IShellFolder2::BindToStorage, IShellFolder::BindToStorage, _win32_IShellFolder_BindToStorage, shell.IShellFolder_BindToStorage, shobjidl_core/IShellFolder2::BindToStorage, shobjidl_core/IShellFolder::BindToStorage
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
 - IShellFolder::BindToStorage
 - shobjidl_core/IShellFolder::BindToStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
 - netshell.dll
api_name:
 - IShellFolder.BindToStorage
 - IShellFolder2.BindToStorage
---

# IShellFolder::BindToStorage


## -description

Requests a pointer to an object's storage interface.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

The address of an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that identifies the subfolder relative to its parent folder. The structure must contain exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure followed by a terminating zero.

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

The optional address of an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object to be used during this operation. If this parameter is not used, set it to <b>NULL</b>. Because support for <i>pbc</i> is optional for folder object implementations, some folders may not support the use of bind contexts.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the requested storage interface. To retrieve an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>, <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>, or <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface pointer, set <i>riid</i> to <b>IID_IStream</b>, <b>IID_IStorage</b>, or <b>IID_IPropertySetStorage</b>, respectively.

### -param ppv [out]

Type: <b>void**</b>

The address that receives the interface pointer specified by <i>riid</i>. If an error occurs, a <b>NULL</b> pointer is returned in this address.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Namespace extensions have the option of allowing applications to bind to an object that represents an item's storage. If this option is supported, <b>IShellFolder::BindToStorage</b> returns a specified interface pointer that can then be used to access the contents of object. See the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtostorage">IMoniker::BindToStorage</a> reference for further discussion.