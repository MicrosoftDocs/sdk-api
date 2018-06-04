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

# IOfflineFilesCache::GetDiskSpaceInformation


## -description


Retrieves the amount of disk space used by the Offline Files cache as well as the space limits applied to cache usage.


## -parameters




### -param pcbVolumeTotal [out]

Receives the size, in bytes, of the volume hosting the Offline Files cache.


### -param pcbLimit [out]

Receives the limit on the maximum amount of bytes that can be stored in the Offline Files cache.


### -param pcbUsed [out]

Receives the current number of bytes used by all files that are pinned and automatically cached in the Offline Files cache.


### -param pcbUnpinnedLimit [out]

Receives the limit on the maximum amount of bytes that can be stored in the Offline Files cache for automatically cached files.


### -param pcbUnpinnedUsed [out]

Receives the current number of bytes used by all automatically cached files in the Offline Files cache.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The cache space limits may be adjusted by an administrator using <a href="https://msdn.microsoft.com/cdbfd5af-000a-4724-8a44-5641b2f75896">IOfflineFilesCache::SetDiskSpaceLimits</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

