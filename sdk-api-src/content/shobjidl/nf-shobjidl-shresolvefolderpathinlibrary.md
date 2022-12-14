---
UID: NF:shobjidl.SHResolveFolderPathInLibrary
title: SHResolveFolderPathInLibrary function (shobjidl.h)
description: Attempts to resolve the target location of a library folder that has been moved or renamed.
helpviewer_keywords: ["SHResolveFolderPathInLibrary","SHResolveFolderPathInLibrary function [Windows Shell]","_shell_SHResolveFolderPathInLibrary","shell.SHResolveFolderPathInLibrary","shobjidl/SHResolveFolderPathInLibrary"]
old-location: shell\SHResolveFolderPathInLibrary.htm
tech.root: shell
ms.assetid: e9c8aacd-9abb-4640-b9ed-1fa417d4d4cc
ms.date: 12/05/2018
ms.keywords: SHResolveFolderPathInLibrary, SHResolveFolderPathInLibrary function [Windows Shell], _shell_SHResolveFolderPathInLibrary, shell.SHResolveFolderPathInLibrary, shobjidl/SHResolveFolderPathInLibrary
req.header: shobjidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHResolveFolderPathInLibrary
 - shobjidl/SHResolveFolderPathInLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - SHResolveFolderPathInLibrary
---

# SHResolveFolderPathInLibrary function


## -description

Attempts to resolve the target location of a library folder that has been moved or renamed.

## -parameters

### -param plib [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>*</b>

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object for which to resolve the target location.

### -param pszFolderPath [in]

Type: <b>PCWSTR</b>

The path of the library folder to locate.

### -param dwTimeout [in]

Type: <b>DWORD</b>

The maximum time, in milliseconds, that the method attempts to locate the folder before returning. If the folder could not be located before the specified time elapses, an error is returned.

### -param ppszResolvedPath [out]

Type: <b>PWSTR*</b>

A pointer to a string that, when this function successfully returns, contains the current path of the library folder specified in <i>plib</i>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an inline helper function that wraps the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-resolvefolder">IShellLibrary::ResolveFolder</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-resolvefolder">IShellLibrary::ResolveFolder</a>