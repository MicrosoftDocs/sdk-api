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

# ISecurityCallContext::get_Item


## -description


Retrieves a specified property in the security call context collection.


## -parameters




### -param name [in]

The name of the property item to be retrieved. See Remarks for information about the available items.


### -param pItem [out]

A reference to the retrieved property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The security call context collection represents a security call context, which provides information about the callers in the chain of calls ending with the current call. For each item in the security call context collection, the following table provides a description, the index name used to retrieve it, and the returned data type of the item.

<table>
<tr>
<th>Item</th>
<th>Description</th>
<th>Index name</th>
<th>Returned type</th>
</tr>
<tr>
<td>Direct Caller
</td>
<td>The immediate caller of the object.</td>
<td>"DirectCaller"
</td>
<td>A <a href="https://msdn.microsoft.com/c6b28695-1b08-490a-8d56-eb55d82f3e7a">SecurityIdentity</a> object
</td>
</tr>
<tr>
<td>Original Caller
</td>
<td>The caller that originated the chain of calls to the object.</td>
<td>"OriginalCaller"
</td>
<td>A <a href="https://msdn.microsoft.com/c6b28695-1b08-490a-8d56-eb55d82f3e7a">SecurityIdentity</a> object
</td>
</tr>
<tr>
<td>Minimum Authentication Level
</td>
<td>The lowest authentication level used in the chain of calls.</td>
<td>"MinAuthenticationLevel"
</td>
<td>A <b>Long</b></td>
</tr>
<tr>
<td>Number of Callers
</td>
<td>The number of callers in the chain of calls to the object.</td>
<td>"NumCallers"
</td>
<td>A <b>Long</b></td>
</tr>
<tr>
<td>Callers
</td>
<td>The callers in the chain of calls that ends with the current call.</td>
<td>"Callers"</td>
<td>A <a href="https://msdn.microsoft.com/164fe12d-eeb3-402f-8aa3-e3545904d9c4">SecurityCallers</a> object
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>
 

 

