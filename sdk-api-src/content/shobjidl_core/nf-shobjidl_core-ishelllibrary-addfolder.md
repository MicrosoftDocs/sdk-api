---
UID: NF:shobjidl_core.IShellLibrary.AddFolder
title: IShellLibrary::AddFolder (shobjidl_core.h)
description: Adds a folder to the library.
helpviewer_keywords: ["AddFolder","AddFolder method [Windows Shell]","AddFolder method [Windows Shell]","IShellLibrary interface","IShellLibrary interface [Windows Shell]","AddFolder method","IShellLibrary.AddFolder","IShellLibrary::AddFolder","_shell_IShellLibrary_AddFolder","shell.IShellLibrary_AddFolder","shobjidl_core/IShellLibrary::AddFolder"]
old-location: shell\IShellLibrary_AddFolder.htm
tech.root: shell
ms.assetid: 7455998a-56a8-4fc1-882b-c0942fd35d8c
ms.date: 12/05/2018
ms.keywords: AddFolder, AddFolder method [Windows Shell], AddFolder method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],AddFolder method, IShellLibrary.AddFolder, IShellLibrary::AddFolder, _shell_IShellLibrary_AddFolder, shell.IShellLibrary_AddFolder, shobjidl_core/IShellLibrary::AddFolder
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
 - IShellLibrary::AddFolder
 - shobjidl_core/IShellLibrary::AddFolder
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
 - IShellLibrary.AddFolder
---

# IShellLibrary::AddFolder


## -description

Adds a folder to the library.

## -parameters

### -param psiLocation [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the folder to be added to the library.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a folder is added to a library it is also added to the <a href="/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> index.

For convenience, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shaddfolderpathtolibrary">SHAddFolderPathToLibrary</a> can be used in place of this method.


#### Examples

The following code example shows the helper function <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shaddfolderpathtolibrary">SHAddFolderPathToLibrary</a>, which wraps this method.


```cpp
//
// From Shobjidl.h
//
__inline HRESULT SHAddFolderPathToLibrary (
    __in IShellLibrary *plib,
    __in PCWSTR pszFolderPath
)
{
    IShellItem *psiFolder;
    
    HRESULT hr = SHCreateItemFromParsingName (
      pszFolderPath, 
      NULL,
      IID_PPV_ARGS(&psiFolder));
    
    if (SUCCEEDED(hr))
    {
        hr = plib->AddFolder (psiFolder);
        psiFolder->Release ();
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-removefolder">IShellLibrary::RemoveFolder</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shaddfolderpathtolibrary">SHAddFolderPathToLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>