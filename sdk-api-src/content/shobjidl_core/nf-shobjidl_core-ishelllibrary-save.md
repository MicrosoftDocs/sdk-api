---
UID: NF:shobjidl_core.IShellLibrary.Save
title: IShellLibrary::Save (shobjidl_core.h)
description: Saves the library to a new Library Description (*.library-ms) file.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","Save method","IShellLibrary.Save","IShellLibrary::Save","Save","Save method [Windows Shell]","Save method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_Save","shell.IShellLibrary_Save","shobjidl_core/IShellLibrary::Save"]
old-location: shell\IShellLibrary_Save.htm
tech.root: shell
ms.assetid: 2a7de829-f0bc-4ace-aed4-83d0611ae292
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],Save method, IShellLibrary.Save, IShellLibrary::Save, Save, Save method [Windows Shell], Save method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_Save, shell.IShellLibrary_Save, shobjidl_core/IShellLibrary::Save
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
 - IShellLibrary::Save
 - shobjidl_core/IShellLibrary::Save
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
 - IShellLibrary.Save
---

# IShellLibrary::Save


## -description

Saves the library to a new Library Description (*.library-ms) file.

## -parameters

### -param psiFolderToSaveIn [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

The  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object  that specifies the folder in which to save the library, or <b>NULL</b> to save the library  with the user's default libraries in the FOLDERID_Libraries known folder.

### -param pszLibraryName [in]

Type: <b>LPCWSTR</b>

The file name under which to save the library. The file name must not include the file name extension; the file name extension is added automatically.

### -param lsf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a></b>

The <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a>  value that specifies how to handle a library name collision.

### -param ppsiSavedTo [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object  that represents the library description file into   which the library was saved.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IShellLibrary::Save</b> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a> create a new library file, and save the file to disk. To save changes made to a library that has an existing library file, call  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-commit">IShellLibrary::Commit</a>.

If the library is saved in the Libraries known folder (FOLDERID_Libraries), the library's location is automatically added to the system index.

For convenience, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a> can be used in place of this method.


#### Examples

The following code example shows the helper function <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>, which wraps this method.


```cpp
//
// from shobjidl.h
//
__inline HRESULT SHSaveLibraryInFolderPath(
    __in IShellLibrary *plib, 
    __in PCWSTR pszFolderPath, 
    __in PCWSTR pszLibraryName, 
    __in LIBRARYSAVEFLAGS lsf, 
    __deref_opt_out PWSTR *ppszSavedToPath
)
{
    if (ppszSavedToPath)
    {
        *ppszSavedToPath = NULL;
    }

    IShellItem *psiFolder;
    HRESULT hr = SHCreateItemFromParsingName(
      pszFolderPath, 
      NULL, 
      IID_PPV_ARGS(&psiFolder));

    if (SUCCEEDED(hr))
    {
        IShellItem *psiSavedTo;
        hr = plib->Save(psiFolder, pszLibraryName, lsf, &psiSavedTo);

        if (SUCCEEDED(hr))
        {
            if (ppszSavedToPath)
            {
                hr = psiSavedTo->GetDisplayName(
                  SIGDN_DESKTOPABSOLUTEPARSING, 
                  ppszSavedToPath);
            }
            psiSavedTo->Release();
        }
        psiFolder->Release();
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>