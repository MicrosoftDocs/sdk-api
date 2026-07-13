---
UID: NF:shobjidl_core.SHSaveLibraryInFolderPath
title: SHSaveLibraryInFolderPath function (shobjidl_core.h)
description: Saves an IShellLibrary object to disk.
helpviewer_keywords: ["SHSaveLibraryInFolderPath","SHSaveLibraryInFolderPath function [Windows Shell]","_shell_SHSaveLibraryInFolderPath","shell.SHSaveLibraryInFolderPath","shobjidl_core/SHSaveLibraryInFolderPath"]
old-location: shell\SHSaveLibraryInFolderPath.htm
tech.root: shell
ms.assetid: 953b209b-fd18-49d0-84d3-ad9b815f2a3a
ms.date: 12/05/2018
ms.keywords: SHSaveLibraryInFolderPath, SHSaveLibraryInFolderPath function [Windows Shell], _shell_SHSaveLibraryInFolderPath, shell.SHSaveLibraryInFolderPath, shobjidl_core/SHSaveLibraryInFolderPath
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
 - SHSaveLibraryInFolderPath
 - shobjidl_core/SHSaveLibraryInFolderPath
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
 - SHSaveLibraryInFolderPath
---

# SHSaveLibraryInFolderPath function


## -description

Saves an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object to disk.

## -parameters

### -param plib [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object to save.

### -param pszFolderPath [in]

Type: <b>PCWSTR</b>

A pointer to the path to the folder in which to save the library.

### -param pszLibraryName [in]

Type: <b>PCWSTR</b>

A pointer to a file name under which to save the library. The file name must not include the file name extension. The file name extension is added automatically.

### -param lsf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a></b>

A value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a> enumeration that specifies how to handle a library name collision.

### -param ppszSavedToPath [out, optional]

Type: <b>PWSTR*</b>

A pointer to a string that, when this function returns successfully, receives the path to the library description file into which the library was saved. If this path is not required, the value of this parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an inline helper function that wraps the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-saveinknownfolder">IShellLibrary::SaveInKnownFolder</a>