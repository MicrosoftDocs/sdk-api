---
UID: NE:virtdisk._CREATE_VIRTUAL_DISK_FLAG
title: CREATE_VIRTUAL_DISK_FLAG (virtdisk.h)
description: Contains virtual hard disk (VHD) creation flags.
helpviewer_keywords: ["CREATE_VIRTUAL_DISK_FLAG","CREATE_VIRTUAL_DISK_FLAG enumeration [VHD]","CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT","CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION","CREATE_VIRTUAL_DISK_FLAG_NONE","CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK","vdssys/CREATE_VIRTUAL_DISK_FLAG","vdssys/CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT","vdssys/CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION","vdssys/CREATE_VIRTUAL_DISK_FLAG_NONE","vdssys/CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK","vhd.create_virtual_disk_flag","virtdisk/CREATE_VIRTUAL_DISK_FLAG","virtdisk/CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT","virtdisk/CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION","virtdisk/CREATE_VIRTUAL_DISK_FLAG_NONE","virtdisk/CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK"]
old-location: vhd\create_virtual_disk_flag.htm
tech.root: VStor
ms.assetid: 35dba6c6-2825-425a-b432-a6ac8ad4ea4b
ms.date: 12/05/2018
ms.keywords: CREATE_VIRTUAL_DISK_FLAG, CREATE_VIRTUAL_DISK_FLAG enumeration [VHD], CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT, CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION, CREATE_VIRTUAL_DISK_FLAG_NONE, CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK, vdssys/CREATE_VIRTUAL_DISK_FLAG, vdssys/CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT, vdssys/CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION, vdssys/CREATE_VIRTUAL_DISK_FLAG_NONE, vdssys/CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK, vhd.create_virtual_disk_flag, virtdisk/CREATE_VIRTUAL_DISK_FLAG, virtdisk/CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT, virtdisk/CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION, virtdisk/CREATE_VIRTUAL_DISK_FLAG_NONE, virtdisk/CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK
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
req.typenames: CREATE_VIRTUAL_DISK_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREATE_VIRTUAL_DISK_FLAG
 - virtdisk/_CREATE_VIRTUAL_DISK_FLAG
 - CREATE_VIRTUAL_DISK_FLAG
 - virtdisk/CREATE_VIRTUAL_DISK_FLAG
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
 - CREATE_VIRTUAL_DISK_FLAG
---

# CREATE_VIRTUAL_DISK_FLAG enumeration


## -description

Contains virtual hard disk (VHD) creation flags.

## -enum-fields

### -field CREATE_VIRTUAL_DISK_FLAG_NONE:0x0

No special creation conditions; system defaults are used.

### -field CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION:0x1

Pre-allocate all physical space necessary for the size of the virtual disk.

### -field CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK:0x2

Take ownership of the source disk during create from source disk, to insure the source disk does not change 
       during the create operation. The source disk must also already be offline or read-only (or both). Ownership is 
       released when create is done. This also has a side-effect of disallowing concurrent create from same source 
       disk. Create will fail if ownership cannot be obtained or if the source disk is not already offline or 
       read-only. This flag is optional, but highly recommended for creates from source disk. No effect for other 
       types of create (no effect for create from source VHD; no effect for create without SourcePath).

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT:0x4

Do not copy initial virtual disk metadata or block states from the parent VHD; this is useful if the parent 
       VHD is a stand-in file and the real parent will be explicitly set later.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field CREATE_VIRTUAL_DISK_FLAG_CREATE_BACKING_STORAGE:0x8

### -field CREATE_VIRTUAL_DISK_FLAG_USE_CHANGE_TRACKING_SOURCE_LIMIT:0x10

### -field CREATE_VIRTUAL_DISK_FLAG_PRESERVE_PARENT_CHANGE_TRACKING_STATE:0x20

### -field CREATE_VIRTUAL_DISK_FLAG_VHD_SET_USE_ORIGINAL_BACKING_STORAGE:0x40

### -field CREATE_VIRTUAL_DISK_FLAG_SPARSE_FILE:0x80

### -field CREATE_VIRTUAL_DISK_FLAG_PMEM_COMPATIBLE:0x100

## -remarks

The <b>CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION</b> flag is used for the creation of a fixed VHD.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
