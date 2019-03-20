---
UID: NF:shobjidl_core.IShellLibrary.LoadLibraryFromKnownFolder
title: IShellLibrary::LoadLibraryFromKnownFolder (shobjidl_core.h)
author: windows-sdk-content
description: Loads the library that is referenced by a KNOWNFOLDERID.
old-location: shell\IShellLibrary_LoadLibraryFromKnownFolder.htm
tech.root: shell
ms.assetid: 3fc1147e-6338-4fec-b20d-db5eb1303fe1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellLibrary interface [Windows Shell],LoadLibraryFromKnownFolder method, IShellLibrary.LoadLibraryFromKnownFolder, IShellLibrary::LoadLibraryFromKnownFolder, LoadLibraryFromKnownFolder, LoadLibraryFromKnownFolder method [Windows Shell], LoadLibraryFromKnownFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_LoadLibraryFromKnownFolder, shell.IShellLibrary_LoadLibraryFromKnownFolder, shobjidl_core/IShellLibrary::LoadLibraryFromKnownFolder
ms.topic: method
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
---

# IShellLibrary::LoadLibraryFromKnownFolder


## -description


Loads  the  library  that is referenced by a  KNOWNFOLDERID.


## -parameters




### -param kfidLibrary [in]

Type: <b>REFKNOWNFOLDERID</b>

The  <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> value that identifies the library to load.


### -param grfMode [in]

Type: <b>DWORD</b>

One or more <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> storage medium flags that specify access and sharing modes for the library object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If  the  <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object  contains a library when this method is called,  that library is overwritten in memory with the new library.

If there is no existing <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object for this library, <a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a> can be  called  in place of this method.


#### Examples

The following code example shows the helper function <a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>, which wraps this method.


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




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/7e682a2e-5140-49ad-88de-ac681025aca4">SHCreateLibrary</a>



<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

