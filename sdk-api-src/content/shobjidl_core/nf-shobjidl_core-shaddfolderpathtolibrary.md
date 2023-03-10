---
UID: NF:shobjidl_core.SHAddFolderPathToLibrary
title: SHAddFolderPathToLibrary function (shobjidl_core.h)
description: Adds a folder to a library.
helpviewer_keywords: ["SHAddFolderPathToLibrary","SHAddFolderPathToLibrary function [Windows Shell]","_shell_SHAddFolderPathToLibrary","shell.SHAddFolderPathToLibrary","shobjidl_core/SHAddFolderPathToLibrary"]
old-location: shell\SHAddFolderPathToLibrary.htm
tech.root: shell
ms.assetid: 308e7905-dfa1-438f-9e7e-f895517e7adb
ms.date: 12/05/2018
ms.keywords: SHAddFolderPathToLibrary, SHAddFolderPathToLibrary function [Windows Shell], _shell_SHAddFolderPathToLibrary, shell.SHAddFolderPathToLibrary, shobjidl_core/SHAddFolderPathToLibrary
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAddFolderPathToLibrary
 - shobjidl_core/SHAddFolderPathToLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHAddFolderPathToLibrary
---

# SHAddFolderPathToLibrary function


## -description

Adds a folder to a library.

## -parameters

### -param plib [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object to which to add the folder.

### -param pszFolderPath [in]

Type: <b>PCWSTR</b>

The folder to add, specified by path.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an inline helper function that wraps the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-addfolder">IShellLibrary::AddFolder</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-addfolder">IShellLibrary::AddFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-removefolder">IShellLibrary::RemoveFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a>