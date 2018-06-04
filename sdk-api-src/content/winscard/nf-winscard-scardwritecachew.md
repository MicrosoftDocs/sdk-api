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

# SCardWriteCacheW function


## -description


The <b>SCardWriteCache</b> function writes a name-value pair from a smart card to the global cache maintained by the <a href="https://msdn.microsoft.com/96434996-88fa-47d3-bb44-3ebb23610b27">Smart Card Resource Manager</a>.


## -parameters




### -param hContext [in]

A handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


### -param CardIdentifier [in]

A pointer to a value that uniquely identifies the smart card from which the name-value pair was read.


### -param FreshnessCounter [in]

The current revision of the cached data.


### -param LookupName [in]

A pointer to a null-terminated string that contains the name portion of the name-value pair to write to the global cache.


### -param Data [in]

A pointer to an array of byte values that contain the value portion of the name-value pair to write to the global cache.


### -param DataLen [in]

The size, in bytes, of the <i>Data</i> buffer.


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
<dt><b>SCARD_W_CACHE_ITEM_TOO_BIG</b></dt>
<dt>0x80100072</dt>
</dl>
</td>
<td width="60%">
The size of the specified name-value pair exceeds the maximum size defined for the global cache.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ffa15036-b6d6-4c0a-8f04-e1900484eb8d">SCardReadCache</a>
 

 

