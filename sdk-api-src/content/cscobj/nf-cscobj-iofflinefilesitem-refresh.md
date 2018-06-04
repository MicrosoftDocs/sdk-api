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

# IOfflineFilesItem::Refresh


## -description


Refreshes any data cached in the object by rereading from the Offline Files cache. 


## -parameters




### -param dwQueryFlags [in]

TBD


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.

<code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the file does not exist in the cache.  This would happen if a file has been deleted from the cache after the file object was first created.




## -remarks



When a file object is first created, its internal data is initialized with information from the Offline Files cache.  It is possible that while an object is held in memory, its true state in the cache can change at any time.  Calling <b>Refresh</b> updates the object with the latest information from the Offline Files cache.




## -see-also




<a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>
 

 

