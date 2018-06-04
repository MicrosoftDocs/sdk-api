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

# SCardReadCacheW function


## -description


The <b>SCardReadCache</b> function retrieves the value portion of a name-value pair from the global cache maintained by the <a href="https://msdn.microsoft.com/96434996-88fa-47d3-bb44-3ebb23610b27">Smart Card Resource Manager</a>.


## -parameters




### -param hContext [in]

A handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


### -param CardIdentifier [in]

A pointer to a value that uniquely identifies a smart card. The name-value pair that this function reads from the global cache is associated with this smart card.


### -param FreshnessCounter [in]

The current revision of the cached data.


### -param LookupName [in]

A pointer to a null-terminated string that contains the name portion of the name-value pair for which to retrieve the value portion.


### -param Data [out]

A pointer to an array of byte values that contain the value portion of the name-value pair specified by the <i>LookupName</i> parameter.


### -param DataLen [out]

A pointer to the size, in bytes, of the <i>Data</i> buffer.


## -returns




						If the function succeeds, it returns <b>SCARD_S_SUCCESS</b>.

If the function fails, it returns one of the following error codes. For more information, see <a href="authentication_return_values.htm">Smart Card Return Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_CACHE_ITEM_NOT_FOUND</b></dt>
<dt>0x80100070</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair was not found in the global cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_CACHE_ITEM_STALE</b></dt>
<dt>0x80100071</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair was older than requested and has been deleted from the cache.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e982e297-6a78-41f4-a81c-d207a96f1dab">SCardWriteCache</a>
 

 

