---
UID: NF:shlobj_core.SHBindToFolderIDListParentEx
title: SHBindToFolderIDListParentEx function (shlobj_core.h)
description: Extends the SHBindToFolderIDListParent function by allowing the caller to specify a bind context.
helpviewer_keywords: ["SHBindToFolderIDListParentEx","SHBindToFolderIDListParentEx function [Windows Shell]","_shell_SHBindToFolderIDListParentEx","shell.SHBindToFolderIDListParentEx","shlobj_core/SHBindToFolderIDListParentEx"]
old-location: shell\SHBindToFolderIDListParentEx.htm
tech.root: shell
ms.assetid: 4f9b68cb-d0ae-45f7-90f5-2db1da3ab599
ms.date: 12/05/2018
ms.keywords: SHBindToFolderIDListParentEx, SHBindToFolderIDListParentEx function [Windows Shell], _shell_SHBindToFolderIDListParentEx, shell.SHBindToFolderIDListParentEx, shlobj_core/SHBindToFolderIDListParentEx
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
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHBindToFolderIDListParentEx
 - shlobj_core/SHBindToFolderIDListParentEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - ext-ms-win-shell-shell32-l1-2-2.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - SHBindToFolderIDListParentEx
---

# SHBindToFolderIDListParentEx function


## -description

Extends the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent">SHBindToFolderIDListParent</a> function by allowing the caller to specify a bind context.

## -parameters

### -param psfRoot [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to a Shell folder object. If <i>psfRoot</i> is <b>NULL</b>, indicates that the IDList passed is relative to the desktop.

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A PIDL to bind to, relative to <i>psfRoot</i>. If <i>psfRoot</i> is <b>NULL</b>, this is an absolute IDList relative to the desktop folder.

### -param ppbc [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object to be used during this operation. If this parameter is not used, set it to <b>NULL</b>, which is equivalent to calling the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent">SHBindToFolderIDListParent</a> function. Because support for <i>pbc</i> is optional for folder object implementations, some folders may not support the use of bind contexts.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID. This is typically IID_IShellFolder or IID_IShellFolder2, but can be anything supported by the target folder.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>, but can be anything supported by the target folder.

### -param ppidlLast [out, optional]

Type: <b>PCUITEMID_CHILD*</b>

A pointer to the last ID of the <i>pidl</i> parameter, and is a child ID relative to the parent folder returned in <i>ppv</i>. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent">SHBindToFolderIDListParent</a>