---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WbioQueryStorageInterface function


## -description


Retrieves a pointer to the <a href="https://msdn.microsoft.com/1cc7ce07-66df-43d9-9db2-50558a0f5f47">WINBIO_STORAGE_INTERFACE</a> structure for the storage adapter.


## -parameters




### -param StorageInterface [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/1cc7ce07-66df-43d9-9db2-50558a0f5f47">WINBIO_STORAGE_INTERFACE</a> structure.


## -returns



If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>StorageInterface</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The Windows Biometric Framework calls this function after loading a storage adapter DLL into memory.
Every storage adapter DLL must therefore implement and export the <b>WbioQueryStorageInterface</b>  function. The function name is case-sensitive, and its spelling and signature must exactly match that provided in the Syntax section.

To be visible to the Windows Biometric Framework, the <b>WbioQueryStorageInterface</b> function must be named in the EXPORTS section of the export definition linker command file for the DLL.



#### Examples

The following pseudocode shows one possible implementation of this function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT
WINAPI
WbioQueryStorageInterface(
    __out PWINBIO_STORAGE_INTERFACE *StorageInterface
    )
{
    *StorageInterface = &amp;g_StorageInterface; 
    return S_OK;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

