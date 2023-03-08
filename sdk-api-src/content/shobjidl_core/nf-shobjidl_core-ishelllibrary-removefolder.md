---
UID: NF:shobjidl_core.IShellLibrary.RemoveFolder
title: IShellLibrary::RemoveFolder (shobjidl_core.h)
description: Removes a folder from the library.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","RemoveFolder method","IShellLibrary.RemoveFolder","IShellLibrary::RemoveFolder","RemoveFolder","RemoveFolder method [Windows Shell]","RemoveFolder method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_RemoveFolder","shell.IShellLibrary_RemoveFolder","shobjidl_core/IShellLibrary::RemoveFolder"]
old-location: shell\IShellLibrary_RemoveFolder.htm
tech.root: shell
ms.assetid: 2ba2c504-e96c-4b56-b2f2-196c0b74c9eb
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],RemoveFolder method, IShellLibrary.RemoveFolder, IShellLibrary::RemoveFolder, RemoveFolder, RemoveFolder method [Windows Shell], RemoveFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_RemoveFolder, shell.IShellLibrary_RemoveFolder, shobjidl_core/IShellLibrary::RemoveFolder
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
 - IShellLibrary::RemoveFolder
 - shobjidl_core/IShellLibrary::RemoveFolder
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
 - IShellLibrary.RemoveFolder
---

# IShellLibrary::RemoveFolder


## -description

Removes a folder from the library.

## -parameters

### -param psiLocation [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the folder to remove.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For convenience, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a> can be used in place of this method.


#### Examples

The following code example shows the helper function <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a>, which wraps this method.


```cpp
//
// from shobjidl.h
//
__inline HRESULT SHRemoveFolderPathFromLibrary(
    __in IShellLibrary *plib,
    __in PCWSTR pszFolderPath)
{
    PIDLIST_ABSOLUTE pidlFolder = 
      SHSimpleIDListFromPath (pszFolderPath);
    HRESULT hr = pidlFolder ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        IShellItem *psiFolder;
        hr = SHCreateItemFromIDList (
          pidlFolder, 
          IID_PPV_ARGS(&psiFolder));

        if (SUCCEEDED(hr))
        {
            hr = plib->RemoveFolder(psiFolder);
            psiFolder->Release();
        }
        CoTaskMemFree(pidlFolder);
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-addfolder">IShellLibrary::AddFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shaddfolderpathtolibrary">SHAddFolderPathToLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>