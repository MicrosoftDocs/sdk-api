---
UID: NF:shobjidl_core.IShellLibrary.AddFolder
title: IShellLibrary::AddFolder
author: windows-sdk-content
description: Adds a folder to the library.
old-location: shell\IShellLibrary_AddFolder.htm
old-project: shell
ms.assetid: 7455998a-56a8-4fc1-882b-c0942fd35d8c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AddFolder, AddFolder method [Windows Shell], AddFolder method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],AddFolder method, IShellLibrary.AddFolder, IShellLibrary::AddFolder, _shell_IShellLibrary_AddFolder, shell.IShellLibrary_AddFolder, shobjidl_core/IShellLibrary::AddFolder
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
 - IShellLibrary.AddFolder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLibrary::AddFolder


## -description


Adds a folder to the library.


## -parameters




### -param psiLocation [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

An <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the folder to be added to the library.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a folder is added to a library it is also added to the <a href="https://msdn.microsoft.com/library/Aa965362(v=VS.85).aspx">Windows Search</a> index.

For convenience, <a href="https://msdn.microsoft.com/308e7905-dfa1-438f-9e7e-f895517e7adb">SHAddFolderPathToLibrary</a> can be used in place of this method.


#### Examples

The following code example shows the helper function <a href="https://msdn.microsoft.com/308e7905-dfa1-438f-9e7e-f895517e7adb">SHAddFolderPathToLibrary</a>, which wraps this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
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
      IID_PPV_ARGS(&amp;psiFolder));
    
    if (SUCCEEDED(hr))
    {
        hr = plib-&gt;AddFolder (psiFolder);
        psiFolder-&gt;Release ();
    }
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/2ba2c504-e96c-4b56-b2f2-196c0b74c9eb">IShellLibrary::RemoveFolder</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/308e7905-dfa1-438f-9e7e-f895517e7adb">SHAddFolderPathToLibrary</a>



<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>



<a href="https://msdn.microsoft.com/34de407c-54f0-4be9-a383-4bf1baa63eef">SHRemoveFolderPathFromLibrary</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

