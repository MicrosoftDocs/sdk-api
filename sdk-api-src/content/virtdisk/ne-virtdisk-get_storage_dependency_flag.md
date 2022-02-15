---
UID: NE:virtdisk._GET_STORAGE_DEPENDENCY_FLAG
title: GET_STORAGE_DEPENDENCY_FLAG (virtdisk.h)
description: Contains virtual hard disk (VHD) storage dependency request flags.
helpviewer_keywords: ["GET_STORAGE_DEPENDENCY_FLAG","GET_STORAGE_DEPENDENCY_FLAG enumeration [VHD]","GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE","GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES","GET_STORAGE_DEPENDENCY_FLAG_NONE","vdssys/GET_STORAGE_DEPENDENCY_FLAG","vdssys/GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE","vdssys/GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES","vdssys/GET_STORAGE_DEPENDENCY_FLAG_NONE","vhd.get_storage_dependency_flag","virtdisk/GET_STORAGE_DEPENDENCY_FLAG","virtdisk/GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE","virtdisk/GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES","virtdisk/GET_STORAGE_DEPENDENCY_FLAG_NONE"]
old-location: vhd\get_storage_dependency_flag.htm
tech.root: VStor
ms.assetid: 6a438edf-698b-4b2d-8864-c97fbf9eaa9f
ms.date: 12/05/2018
ms.keywords: GET_STORAGE_DEPENDENCY_FLAG, GET_STORAGE_DEPENDENCY_FLAG enumeration [VHD], GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE, GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES, GET_STORAGE_DEPENDENCY_FLAG_NONE, vdssys/GET_STORAGE_DEPENDENCY_FLAG, vdssys/GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE, vdssys/GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES, vdssys/GET_STORAGE_DEPENDENCY_FLAG_NONE, vhd.get_storage_dependency_flag, virtdisk/GET_STORAGE_DEPENDENCY_FLAG, virtdisk/GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE, virtdisk/GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES, virtdisk/GET_STORAGE_DEPENDENCY_FLAG_NONE
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
targetos: Windows
req.typenames: GET_STORAGE_DEPENDENCY_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GET_STORAGE_DEPENDENCY_FLAG
 - virtdisk/_GET_STORAGE_DEPENDENCY_FLAG
 - GET_STORAGE_DEPENDENCY_FLAG
 - virtdisk/GET_STORAGE_DEPENDENCY_FLAG
dev_langs:
 - c++
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
---

# GET_STORAGE_DEPENDENCY_FLAG enumeration


## -description

Contains virtual hard disk (VHD) storage dependency request flags.

## -enum-fields

### -field GET_STORAGE_DEPENDENCY_FLAG_NONE:0x00000000

No flags specified.

### -field GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES:0x00000001

Return information for volumes or disks hosting the volume specified.

### -field GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE:0x00000002

The handle provided is to a disk, not a volume or file.

## -remarks

If the <b>GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES</b> flag is not set, the <a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation">GetStorageDependencyInformation</a> function returns information about the volumes or disks being hosted by  the volume or disk specified. For example, if the VHD file C:\file.vhd defines the virtual drive D, setting the <b>GET_STORAGE_DEPENDENCY_FLAG_HOST_VOLUMES</b> flag will retrieve information about the C: volume. If not, information about the virtual D: volume will be retrieved.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
