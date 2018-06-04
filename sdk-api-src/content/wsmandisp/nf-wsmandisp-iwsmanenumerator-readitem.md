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

# IWSManEnumerator::ReadItem


## -description


Retrieves an item from the  resource and  returns an XML representation of the item.


## -parameters




### -param resource [out]

The XML representation of the item.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To start an enumeration, use <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession.Enumerate</a>. To perform a WS-Eventing:Pull operation that continues reading items in the enumeration, use <b>IWSManEnumerator.ReadItem</b>.

To limit the number of items that are read, set the <a href="https://msdn.microsoft.com/1675ba12-a0c7-4e59-a013-2109780e8afe">Session.BatchItems</a> property.

Be aware that freeing the enumeration object clears pending enumeration requests.




## -see-also




<a href="https://msdn.microsoft.com/4280ecb8-2449-41bd-868a-785e8ac3b3d5">Enumerator.ReadItem</a>



<a href="https://msdn.microsoft.com/c7afac5d-946f-49ec-a7d0-de558ed2144b">IWSManEnumerator</a>
 

 

