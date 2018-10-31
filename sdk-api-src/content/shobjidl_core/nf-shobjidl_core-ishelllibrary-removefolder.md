---
UID: NF:shobjidl_core.IShellLibrary.RemoveFolder
title: IShellLibrary::RemoveFolder
author: windows-sdk-content
description: Removes a folder from the library.
old-location: shell\IShellLibrary_RemoveFolder.htm
tech.root: shell
ms.assetid: 2ba2c504-e96c-4b56-b2f2-196c0b74c9eb
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IShellLibrary interface [Windows Shell],RemoveFolder method, IShellLibrary.RemoveFolder, IShellLibrary::RemoveFolder, RemoveFolder, RemoveFolder method [Windows Shell], RemoveFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_RemoveFolder, shell.IShellLibrary_RemoveFolder, shobjidl_core/IShellLibrary::RemoveFolder
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IShellLibrary.RemoveFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLibrary::RemoveFolder


## -description


Removes a folder from the library.


## -parameters




### -param psiLocation [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

An <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the folder to remove.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For convenience, <a href="https://msdn.microsoft.com/34de407c-54f0-4be9-a383-4bf1baa63eef">SHRemoveFolderPathFromLibrary</a> can be used in place of this method.


#### Examples

The following code example shows the helper function <a href="https://msdn.microsoft.com/34de407c-54f0-4be9-a383-4bf1baa63eef">SHRemoveFolderPathFromLibrary</a>, which wraps this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
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
          IID_PPV_ARGS(&amp;psiFolder));

        if (SUCCEEDED(hr))
        {
            hr = plib-&gt;RemoveFolder(psiFolder);
            psiFolder-&gt;Release();
        }
        CoTaskMemFree(pidlFolder);
    }
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/7455998a-56a8-4fc1-882b-c0942fd35d8c">IShellLibrary::AddFolder</a>



<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/308e7905-dfa1-438f-9e7e-f895517e7adb">SHAddFolderPathToLibrary</a>



<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>



<a href="https://msdn.microsoft.com/34de407c-54f0-4be9-a383-4bf1baa63eef">SHRemoveFolderPathFromLibrary</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

