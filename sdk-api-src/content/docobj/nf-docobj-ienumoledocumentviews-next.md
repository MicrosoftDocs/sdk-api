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

# IEnumOleDocumentViews::Next


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param cViews [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

If <i>pcFetched</i> is <b>NULL</b>, this parameter must be 1.


### -param rgpView [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>, and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> through each pointer enumerated. If <i>cViews</i> is greater than 1, the caller must also pass a non-<b>NULL</b> pointer passed to <i>pcFetched</i> to know how many pointers to release.


### -param pcFetched [in, out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested. This parameter can be <b>NULL</b>, in which case the <i>cViews</i> parameter must be 1.


## -returns



If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -remarks



E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the <i>rgpView</i> array are valid and no calls to Release are required. 




## -see-also




<a href="https://msdn.microsoft.com/cd8fa8b8-17b1-4d77-9611-473725899351">IEnumOleDocumentViews</a>



<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>
 

 

