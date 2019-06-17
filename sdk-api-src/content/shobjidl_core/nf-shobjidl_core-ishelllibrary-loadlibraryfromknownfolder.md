---
UID: NF:shobjidl_core.IShellLibrary.LoadLibraryFromKnownFolder
title: IShellLibrary::LoadLibraryFromKnownFolder (shobjidl_core.h)
author: windows-sdk-content
description: Loads the library that is referenced by a KNOWNFOLDERID.
old-location: shell\IShellLibrary_LoadLibraryFromKnownFolder.htm
tech.root: shell
ms.assetid: 3fc1147e-6338-4fec-b20d-db5eb1303fe1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],LoadLibraryFromKnownFolder method, IShellLibrary.LoadLibraryFromKnownFolder, IShellLibrary::LoadLibraryFromKnownFolder, LoadLibraryFromKnownFolder, LoadLibraryFromKnownFolder method [Windows Shell], LoadLibraryFromKnownFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_LoadLibraryFromKnownFolder, shell.IShellLibrary_LoadLibraryFromKnownFolder, shobjidl_core/IShellLibrary::LoadLibraryFromKnownFolder
ms.topic: method
f1_keywords: ["shobjidl_core/IShellLibrary.LoadLibraryFromKnownFolder"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.LoadLibraryFromKnownFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellLibrary::LoadLibraryFromKnownFolder


## -description


Loads  the  library  that is referenced by a  KNOWNFOLDERID.


## -parameters




### -param kfidLibrary [in]

Type: <b>REFKNOWNFOLDERID</b>

The  <a href="https://docs.microsoft.com/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> value that identifies the library to load.


### -param grfMode [in]

Type: <b>DWORD</b>

One or more <a href="https://docs.microsoft.com/windows/desktop/Stg/stgm-constants">STGM</a> storage medium flags that specify access and sharing modes for the library object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If  the  <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object  contains a library when this method is called,  that library is overwritten in memory with the new library.

If there is no existing <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object for this library, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a> can be  called  in place of this method.


#### Examples

The following code example shows the helper function <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>, which wraps this method.


```cpp
//
// from shobjidl.h
//
__inline HRESULT SHLoadLibraryFromKnownFolder(
    __in REFKNOWNFOLDERID kfidLibrary, 
    __in DWORD grfMode, 
    __in REFIID riid, 
    __deref_out void **ppv)
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
        hr = plib->LoadLibraryFromKnownFolder(kfidLibrary, grfMode);
        if (SUCCEEDED(hr))
        {
            hr = plib->QueryInterface(riid, ppv);
        }
        plib->Release();
    }
    return hr;}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>
 

 

