---
UID: NE:virtdisk._GET_STORAGE_DEPENDENCY_FLAG
title: "_GET_STORAGE_DEPENDENCY_FLAG"
author: windows-sdk-content
description: Contains virtual hard disk (VHD) storage dependency request flags.
old-location: vhd\get_storage_dependency_flag.htm
tech.root: VStor
ms.assetid: 6a438edf-698b-4b2d-8864-c97fbf9eaa9f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GET_STORAGE_DEPENDENCY_FLAG, GET_STORAGE_DEPENDENCY_FLAG enumeration [VHD], GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE, GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES, GET_STORAGE_DEPENDENCY_FLAG_NONE, _GET_STORAGE_DEPENDENCY_FLAG, vdssys/GET_STORAGE_DEPENDENCY_FLAG, vdssys/GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE, vdssys/GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES, vdssys/GET_STORAGE_DEPENDENCY_FLAG_NONE, vhd.get_storage_dependency_flag, virtdisk/GET_STORAGE_DEPENDENCY_FLAG, virtdisk/GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE, virtdisk/GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES, virtdisk/GET_STORAGE_DEPENDENCY_FLAG_NONE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - GET_STORAGE_DEPENDENCY_FLAG
product: Windows
targetos: Windows
req.typenames: GET_STORAGE_DEPENDENCY_FLAG
req.redist: 
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
 

 

