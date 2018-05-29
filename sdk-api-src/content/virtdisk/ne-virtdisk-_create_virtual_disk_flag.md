---
UID: NE:virtdisk._CREATE_VIRTUAL_DISK_FLAG
title: "_CREATE_VIRTUAL_DISK_FLAG"
author: windows-sdk-content
description: Contains virtual hard disk (VHD) creation flags.
old-location: vhd\create_virtual_disk_flag.htm
old-project: VStor
ms.assetid: 35dba6c6-2825-425a-b432-a6ac8ad4ea4b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CREATE_VIRTUAL_DISK_FLAG, CREATE_VIRTUAL_DISK_FLAG enumeration [VHD], CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT, CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION, CREATE_VIRTUAL_DISK_FLAG_NONE, CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK, _CREATE_VIRTUAL_DISK_FLAG, vhd.create_virtual_disk_flag, virtdisk/CREATE_VIRTUAL_DISK_FLAG, virtdisk/CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT, virtdisk/CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION, virtdisk/CREATE_VIRTUAL_DISK_FLAG_NONE, virtdisk/CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: virtdisk.h
req.include-header: Windows.h
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
req.typenames: CREATE_VIRTUAL_DISK_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	VirtDisk.h
api_name:
-	CREATE_VIRTUAL_DISK_FLAG
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# _CREATE_VIRTUAL_DISK_FLAG enumeration


## -description


Contains virtual hard disk (VHD) creation flags.


## -enum-fields




### -field CREATE_VIRTUAL_DISK_FLAG_NONE

No special creation conditions; system defaults are used.


### -field CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION

Pre-allocate all physical space necessary for the size of the virtual disk.


### -field CREATE_VIRTUAL_DISK_FLAG_PREVENT_WRITES_TO_SOURCE_DISK

Take ownership of the source disk during create from source disk, to insure the source disk does not change 
       during the create operation. The source disk must also already be offline or read-only (or both). Ownership is 
       released when create is done. This also has a side-effect of disallowing concurrent create from same source 
       disk. Create will fail if ownership cannot be obtained or if the source disk is not already offline or 
       read-only. This flag is optional, but highly recommended for creates from source disk. No effect for other 
       types of create (no effect for create from source VHD; no effect for create without SourcePath).

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field CREATE_VIRTUAL_DISK_FLAG_DO_NOT_COPY_METADATA_FROM_PARENT

Do not copy initial virtual disk metadata or block states from the parent VHD; this is useful if the parent 
       VHD is a stand-in file and the real parent will be explicitly set later.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field CREATE_VIRTUAL_DISK_FLAG_CREATE_BACKING_STORAGE


### -field CREATE_VIRTUAL_DISK_FLAG_USE_CHANGE_TRACKING_SOURCE_LIMIT


### -field CREATE_VIRTUAL_DISK_FLAG_PRESERVE_PARENT_CHANGE_TRACKING_STATE


### -field CREATE_VIRTUAL_DISK_FLAG_VHD_SET_USE_ORIGINAL_BACKING_STORAGE


### -field CREATE_VIRTUAL_DISK_FLAG_SPARSE_FILE


### -field CREATE_VIRTUAL_DISK_FLAG_PMEM_COMPATIBLE




## -remarks



The <b>CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION</b> flag is used for the creation of a fixed VHD.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

