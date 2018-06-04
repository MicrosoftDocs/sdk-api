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

# _GET_STORAGE_DEPENDENCY_FLAG enumeration


## -description


Contains virtual hard disk (VHD) storage dependency request flags.


## -enum-fields




### -field GET_STORAGE_DEPENDENCY_FLAG_NONE

No flags specified.


### -field GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES

Return information for volumes or disks hosting the volume specified. 


### -field GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE

The handle provided is to a disk, not a volume or file.


## -remarks



If the <b>GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES</b> flag is not set, the <a href="https://msdn.microsoft.com/9ed3ec7c-5e50-4e81-bba7-798f2fbcf29d">GetStorageDependencyInformation</a> function returns information about the volumes or disks being hosted by  the volume or disk specified. For example, if the VHD file C:\file.vhd defines the virtual drive D, setting the <b>GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES</b> flag will retrieve information about the C: volume. If not, information about the virtual D: volume will be retrieved.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

