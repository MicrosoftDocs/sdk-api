---
UID: NF:shlobj_core.SHBindToObject
title: SHBindToObject function (shlobj_core.h)
description: Retrieves and binds to a specified object by using the Shell namespace IShellFolder::BindToObject method.
helpviewer_keywords: ["SHBindToObject","SHBindToObject function [Windows Shell]","_shell_SHBindToObject","shell.SHBindToObject","shlobj_core/SHBindToObject"]
old-location: shell\SHBindToObject.htm
tech.root: shell
ms.assetid: acc16097-8301-4118-8cb5-00aa2705306a
ms.date: 12/05/2018
ms.keywords: SHBindToObject, SHBindToObject function [Windows Shell], _shell_SHBindToObject, shell.SHBindToObject, shlobj_core/SHBindToObject
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHBindToObject
 - shlobj_core/SHBindToObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHBindToObject
---

# SHBindToObject function


## -description

Retrieves and binds to a specified object by using the Shell namespace <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> method.

## -parameters

### -param psf

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>. This parameter can be <b>NULL</b>.   If <i>psf</i> is <b>NULL</b>,  this indicates 
parameter <i>pidl</i> is relative to the desktop. In this case, <i>pidl</i> must specify an absolute <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

### -param pidl

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to a constant <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> to bind to that is relative to <i>psf</i>. If <i>psf</i> is <b>NULL</b>, this is an absolute <b>ITEMIDLIST</b> relative to the desktop folder.

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object to be used during this operation. If this parameter is not used, set it to <b>NULL</b>. Because support for <i>pbc</i> is optional for folder object implementations, some folders may not support the use of bind contexts.

### -param riid

Type: <b>REFIID</b>

Identifier of the interface to return.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer as specified in <i>riid</i> to the bound object. If an error occurs, contains a <b>NULL</b> pointer.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  This is a helper function that gets the desktop object by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder">SHGetDesktopFolder</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a>