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

# IEnumConnections::Next


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param cConnections [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.


### -param rgcd [out]

An array of enumerated items.

The enumerator is responsible for allocating any memory, and the caller is responsible for freeing it. If <i>celt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pceltFetched</i> to know how many pointers to release.


### -param pcFetched






#### - lpcFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.


## -returns



If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -remarks



After this method returns successfully, the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> (see the <b>pUnk</b> member of <a href="https://msdn.microsoft.com/23312f89-2985-402d-aae4-cd7388137153">CONNECTDATA</a>) for each element in the array. If <i>cConnections</i> is greater than one, the caller must also pass a non-NULL pointer to <i>lpcFetched</i> to get the number of pointers it has to be released.

E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the array are valid on exit, and therefore no release is required.




## -see-also




<a href="https://msdn.microsoft.com/23312f89-2985-402d-aae4-cd7388137153">CONNECTDATA</a>



<a href="https://msdn.microsoft.com/464966c1-e4e9-4b58-9e41-48de408f572f">IEnumConnections</a>
 

 

