---
UID: NF:shobjidl_core.IShellLibrary.LoadLibraryFromItem
title: IShellLibrary::LoadLibraryFromItem (shobjidl_core.h)
description: Loads the library from a specified library definition file.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","LoadLibraryFromItem method","IShellLibrary.LoadLibraryFromItem","IShellLibrary::LoadLibraryFromItem","LoadLibraryFromItem","LoadLibraryFromItem method [Windows Shell]","LoadLibraryFromItem method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_LoadLibraryFromItem","shell.IShellLibrary_LoadLibraryFromItem","shobjidl_core/IShellLibrary::LoadLibraryFromItem"]
old-location: shell\IShellLibrary_LoadLibraryFromItem.htm
tech.root: shell
ms.assetid: 5dd2c197-8846-481f-b51e-ea0a93fd5e9b
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],LoadLibraryFromItem method, IShellLibrary.LoadLibraryFromItem, IShellLibrary::LoadLibraryFromItem, LoadLibraryFromItem, LoadLibraryFromItem method [Windows Shell], LoadLibraryFromItem method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_LoadLibraryFromItem, shell.IShellLibrary_LoadLibraryFromItem, shobjidl_core/IShellLibrary::LoadLibraryFromItem
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
 - IShellLibrary::LoadLibraryFromItem
 - shobjidl_core/IShellLibrary::LoadLibraryFromItem
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
 - IShellLibrary.LoadLibraryFromItem
---

# IShellLibrary::LoadLibraryFromItem


## -description

Loads the library from a specified library definition file.

## -parameters

### -param psiLibrary [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object for the library definition file to load. An error is returned if this object is not a library.

### -param grfMode [in]

Type: <b>DWORD</b>

One or more <a href="/windows/desktop/Stg/stgm-constants">STGM</a> storage medium flags that specify access and sharing modes for the library object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method is called on an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object that is already loaded, the contents of that object are overwritten in memory with the new information.

If there is no existing library object, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a> can be called in place of this method.


#### Examples

The following code example shows the helper function <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>, which wraps this method.


```cpp
//
// from shobjidl.h
//
__inline HRESULT SHLoadLibraryFromItem(
    __in IShellItem *psiLibrary,
    __in DWORD grfMode,
    __in REFIID riid,
    __deref_out void **ppv
)
{
    *ppv = NULL;
    IShellLibrary *plib;

    HRESULT hr = CoCreateInstance(
      CLSID_ShellLibrary, 
      NULL, 
      CLSCTX_INPROC_SERVER, 
      IID_PPV_ARGS(&plib));

    if (SUCCEEDED(hr))
    {
        hr = plib->LoadLibraryFromItem (psiLibrary, grfMode);
        if (SUCCEEDED(hr))
        {
            hr = plib->QueryInterface (riid, ppv);
        }
        plib->Release();
    }
    return hr;
}

```


The following code example shows the helper function <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>, which wraps this method.


```cpp
//
// from shobjidl.h
//
__inline HRESULT SHLoadLibraryFromParsingName(
    __in PCWSTR pszParsingName,
    __in DWORD grfMode,
    __in REFIID riid,
    __deref_out void **ppv
)
{
    *ppv = NULL;
    IShellItem *psiLibrary;
    HRESULT hr = SHCreateItemFromParsingName (
      pszParsingName, 
      NULL, 
      IID_PPV_ARGS(&psiLibrary));

    if (SUCCEEDED(hr))
    {
        hr = SHLoadLibraryFromItem (psiLibrary, grfMode, riid, ppv);
        psiLibrary->Release();
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>