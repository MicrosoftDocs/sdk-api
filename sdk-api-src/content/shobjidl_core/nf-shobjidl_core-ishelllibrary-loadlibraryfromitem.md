---
UID: NF:shobjidl_core.IShellLibrary.LoadLibraryFromItem
title: IShellLibrary::LoadLibraryFromItem
author: windows-sdk-content
description: Loads the library from a specified library definition file.
old-location: shell\IShellLibrary_LoadLibraryFromItem.htm
old-project: shell
ms.assetid: 5dd2c197-8846-481f-b51e-ea0a93fd5e9b
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IShellLibrary interface [Windows Shell],LoadLibraryFromItem method, IShellLibrary.LoadLibraryFromItem, IShellLibrary::LoadLibraryFromItem, LoadLibraryFromItem, LoadLibraryFromItem method [Windows Shell], LoadLibraryFromItem method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_LoadLibraryFromItem, shell.IShellLibrary_LoadLibraryFromItem, shobjidl_core/IShellLibrary::LoadLibraryFromItem
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.LoadLibraryFromItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLibrary::LoadLibraryFromItem


## -description


Loads the library from a specified library definition file.


## -parameters




### -param psiLibrary [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

An <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object for the library definition file to load. An error is returned if this object is not a library.


### -param grfMode [in]

Type: <b>DWORD</b>

One or more <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> storage medium flags that specify access and sharing modes for the library object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method is called on an <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object that is already loaded, the contents of that object are overwritten in memory with the new information.

If there is no existing library object, <a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a> can be called in place of this method.


#### Examples

The following code example shows the helper function <a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>, which wraps this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
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
      IID_PPV_ARGS(&amp;plib));

    if (SUCCEEDED(hr))
    {
        hr = plib-&gt;LoadLibraryFromItem (psiLibrary, grfMode);
        if (SUCCEEDED(hr))
        {
            hr = plib-&gt;QueryInterface (riid, ppv);
        }
        plib-&gt;Release();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
The following code example shows the helper function <a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>, which wraps this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
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
      IID_PPV_ARGS(&amp;psiLibrary));

    if (SUCCEEDED(hr))
    {
        hr = SHLoadLibraryFromItem (psiLibrary, grfMode, riid, ppv);
        psiLibrary-&gt;Release();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

