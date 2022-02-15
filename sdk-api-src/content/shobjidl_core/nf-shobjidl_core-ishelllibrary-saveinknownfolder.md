---
UID: NF:shobjidl_core.IShellLibrary.SaveInKnownFolder
title: IShellLibrary::SaveInKnownFolder (shobjidl_core.h)
description: Saves the library to a new file in a specified known folder.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","SaveInKnownFolder method","IShellLibrary.SaveInKnownFolder","IShellLibrary::SaveInKnownFolder","SaveInKnownFolder","SaveInKnownFolder method [Windows Shell]","SaveInKnownFolder method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_SaveInKnownFolder","shell.IShellLibrary_SaveInKnownFolder","shobjidl_core/IShellLibrary::SaveInKnownFolder"]
old-location: shell\IShellLibrary_SaveInKnownFolder.htm
tech.root: shell
ms.assetid: 3a6fa57f-808d-4893-a01c-f192355f8989
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],SaveInKnownFolder method, IShellLibrary.SaveInKnownFolder, IShellLibrary::SaveInKnownFolder, SaveInKnownFolder, SaveInKnownFolder method [Windows Shell], SaveInKnownFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SaveInKnownFolder, shell.IShellLibrary_SaveInKnownFolder, shobjidl_core/IShellLibrary::SaveInKnownFolder
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLibrary::SaveInKnownFolder
 - shobjidl_core/IShellLibrary::SaveInKnownFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.SaveInKnownFolder
---

# IShellLibrary::SaveInKnownFolder


## -description

Saves the library to a new file in a specified known folder.

## -parameters

### -param kfidToSaveIn [in]

Type: <b>REFKNOWNFOLDERID</b>

The ID of the known folder in which to save the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object.
               
For more information, see <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.

### -param pszLibraryName [in]

Type: <b>LPCWSTR</b>

The file name under which to save the library. The file name must not include the file name extension; the file name extension is added automatically.

### -param lsf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a></b>

The <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a>  value that specifies how to handle a library name collision.

### -param ppsiSavedTo [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object  that represents the library description file into    which the library was saved.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a> create a new library file, and save the file to disk.
            
To save changes made to a library that has an existing library file, call  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-commit">IShellLibrary::Commit</a>.
         

If the library is saved in the Libraries known folder (FOLDERID_Libraries), the library's location is automatically added to the system index.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>