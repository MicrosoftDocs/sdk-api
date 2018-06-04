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

# IOfflineFilesPinInfo2::IsPartlyPinned


## -description


Determines whether the item is partly pinned.


## -parameters




### -param pbPartlyPinned [out]

Receives <b>TRUE</b> if the item has some child content that is pinned in the Offline Files cache, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Only container items, such as directories and shares, can be partly pinned. An item is partly pinned if the item itself is not pinned, but it contains pinned items. The item could contain autocached or transparently cached items in addition to the pinned items.




## -see-also




<a href="https://msdn.microsoft.com/6005d755-5e1b-4eba-95a2-b6c9c00b1a64">IOfflineFilesCache::Pin</a>



<a href="https://msdn.microsoft.com/b2e8ca73-4186-4971-b5be-41ecfc6b5e4a">IOfflineFilesGhostInfo::IsGhosted</a>



<a href="https://msdn.microsoft.com/80aa7e38-dbd7-42c6-b4b8-df4f104dfdc8">IOfflineFilesPinInfo2</a>



<a href="https://msdn.microsoft.com/7f8656e0-0f24-46a0-81b7-62067b0d4c21">IOfflineFilesTransparentCacheInfo::IsTransparentlyCached</a>
 

 

