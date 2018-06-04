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

# PxeProviderQueryIndex function


## -description


Returns the index of the specified provider in the list of registered providers.


## -parameters




### -param pszProviderName [in]

Friendly name for the provider from the call to the 
      <a href="https://msdn.microsoft.com/2b377855-dae7-47cb-925a-9ee0a9265f83">PxeProviderRegister</a> function.


### -param puIndex [out]

Address of a <b>ULONG</b> that will receive the index of the provider.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



If a provider wants to insert itself in the list of registered providers in a specific order (that is, wants to 
    service client requests before or after a certain provider), it can query the index of another provider and then use 
    the returned index to decide its own location.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
// Suppose Provider wants to handle requests after BINLSVC has rejected them.
//
dwError = PxeProviderQueryIndex(L"BINLSVC", &amp;Index);

if (dwError == ERROR_SUCCESS)
{
 if (PxeProviderRegister(L"MYPROV",
                         L"C:\\MyDir\\MyProv.DLL",
                         PXE_REG_INDEX_BOTTOM,
                         Index + 1,              // Add after BINLSVC
                         &amp;hKey) != ERROR_SUCCESS)
 {
  // Handle Error
 }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2b377855-dae7-47cb-925a-9ee0a9265f83">PxeProviderRegister</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

