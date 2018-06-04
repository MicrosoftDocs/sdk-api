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

# IOfflineFilesTransparentCacheInfo::IsTransparentlyCached


## -description


Determines whether the item is transparently cached.


## -parameters




### -param pbTransparentlyCached [out]

A pointer to a variable that receives <b>TRUE</b> if the item is transparently cached, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



A transparently cached item is cached locally. However, it can be accessed only when the server is available and the user is online with respect to that server. If the cached version of the file matches the currect version of the file on the server, requests to read data will be satisfied from the cache rather than requesting the data from the server.




## -see-also




<a href="https://msdn.microsoft.com/59bd7a71-0189-4c4d-a737-e6a3f09a533d">IOfflineFilesEvents3::TransparentCacheItemNotify</a>



<a href="https://msdn.microsoft.com/49c8213c-e8a1-4cb8-9b58-120fc0982b7b">IOfflineFilesTransparentCacheInfo</a>
 

 

