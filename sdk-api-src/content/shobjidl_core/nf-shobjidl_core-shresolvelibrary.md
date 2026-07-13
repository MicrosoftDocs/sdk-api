---
UID: NF:shobjidl_core.SHResolveLibrary
title: SHResolveLibrary function (shobjidl_core.h)
description: Resolves all locations in a library, even those locations that have been moved or renamed.
helpviewer_keywords: ["SHResolveLibrary","SHResolveLibrary function [Windows Shell]","_shell_SHResolveLibrary","shell.SHResolveLibrary","shobjidl_core/SHResolveLibrary"]
old-location: shell\SHResolveLibrary.htm
tech.root: shell
ms.assetid: a8730c09-f872-4bf8-9482-9dd5af31b509
ms.date: 12/05/2018
ms.keywords: SHResolveLibrary, SHResolveLibrary function [Windows Shell], _shell_SHResolveLibrary, shell.SHResolveLibrary, shobjidl_core/SHResolveLibrary
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHResolveLibrary
 - shobjidl_core/SHResolveLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - SHResolveLibrary
---

# SHResolveLibrary function


## -description

Resolves all locations in a library, even those locations that have been moved or renamed.

## -parameters

### -param psiLibrary [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the library.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function can block the calling thread for as long as it takes to resolve all the locations in the specified library. Because it blocks the thread from which it is called, it should not be called from a thread that also handles user interface interactions.

This function resolves all locations in the specified library in a single call. To resolve an individual location in a library, see the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-resolvefolder">IShellLibrary::ResolveFolder</a> method or the <a href="/windows/desktop/api/shobjidl/nf-shobjidl-shresolvefolderpathinlibrary">SHResolveFolderPathInLibrary</a> function.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-resolvefolder">IShellLibrary::ResolveFolder</a>