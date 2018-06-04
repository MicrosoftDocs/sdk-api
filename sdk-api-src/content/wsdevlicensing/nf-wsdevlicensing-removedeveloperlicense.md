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

# RemoveDeveloperLicense function


## -description


Removes a developer license.


## -parameters




### -param hwndParent [in, optional]

The handler to the parent window.


## -returns



Returns an <a href="https://msdn.microsoft.com/8613f5d5-3b3b-470c-9ad8-c1941ef429cd">HResult structure</a> with any error codes that occurred.




## -remarks



The following is a list of common error codes that this function returns:

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The function succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more arguments are invalid.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Insufficient memory.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</td>
<td>The license was not found.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NOT_AUTHENTICATED)</td>
<td>The call requires authentication.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NETWORK_UNREACHABLE)</td>
<td>The network can’t be reached.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</td>
<td>The caller doesn’t have access to the resource (license).</td>
</tr>
</table>
 



