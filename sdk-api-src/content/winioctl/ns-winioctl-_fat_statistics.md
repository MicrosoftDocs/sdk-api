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

# _FAT_STATISTICS structure


## -description


Contains statistical information from the FAT file system.


## -struct-fields




### -field CreateHits

The number of create operations.


### -field SuccessfulCreates

The number of successful create operations.


### -field FailedCreates

The number of failed create operations.


### -field NonCachedReads

The number of read operations that were not cached.


### -field NonCachedReadBytes

The number of bytes read from a file that were not cached.


### -field NonCachedWrites

The number of write operations that were not cached.


### -field NonCachedWriteBytes

The number of bytes written to a file that were not cached.


### -field NonCachedDiskReads

The number of read operations that were not cached. This value includes sub-read operations.


### -field NonCachedDiskWrites

The number of write operations that were not cached. This value includes sub-write operations.


## -see-also




<a href="https://msdn.microsoft.com/fc33e967-fbc0-4f98-9b6c-2d6ac103a256">EXFAT_STATISTICS</a>



<a href="https://msdn.microsoft.com/ff8c7dfe-da7f-4ee2-9a54-613e0cd3e1e2">FILESYSTEM_STATISTICS</a>
 

 

