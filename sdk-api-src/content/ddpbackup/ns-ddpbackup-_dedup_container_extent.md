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

# _DEDUP_CONTAINER_EXTENT structure


## -description


A logical container file may be stored in a single segment or multiple segments in the backup store. 
    <b>DEDUP_CONTAINER_EXTENT</b> represents a single 
    extent of a specific container file as stored in the backup store. The extent may be the full container file or a 
    portion of the file.


## -struct-fields




### -field ContainerIndex

The index in the container list passed to 
      <a href="https://msdn.microsoft.com/25871056-5833-40DA-9C5B-690DCAB16E5C">IDedupReadFileCallback::OrderContainersRestore</a> 
      to which this container extent structure corresponds.


### -field StartOffset

Offset, in bytes, from the beginning of the container to the beginning of the extent.


### -field Length

Length, in bytes, of the extent.


## -remarks



For example, in an incremental backup scheme, the container may reside in the store either as one complete file 
     generated in a full backup, or as multiple incremental files that contain changes in the file since the previous 
     backup.




## -see-also




<a href="https://msdn.microsoft.com/25871056-5833-40DA-9C5B-690DCAB16E5C">IDedupReadFileCallback::OrderContainersRestore</a>
 

 

