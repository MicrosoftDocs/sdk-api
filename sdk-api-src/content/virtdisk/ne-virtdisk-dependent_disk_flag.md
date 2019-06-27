---
UID: NE:virtdisk._DEPENDENT_DISK_FLAG
title: DEPENDENT_DISK_FLAG (virtdisk.h)
author: windows-sdk-content
description: Contains virtual hard disk (VHD) dependency information flags.
old-location: vhd\dependent_disk_flag.htm
tech.root: VStor
ms.assetid: f22bcf17-59fd-4a05-9516-2e14f173ed33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DEPENDENT_DISK_FLAG, DEPENDENT_DISK_FLAG enumeration [VHD], DEPENDENT_DISK_FLAG_FULLY_ALLOCATED, DEPENDENT_DISK_FLAG_MULT_BACKING_FILES, DEPENDENT_DISK_FLAG_NONE, DEPENDENT_DISK_FLAG_NO_DRIVE_LETTER, DEPENDENT_DISK_FLAG_NO_HOST_DISK, DEPENDENT_DISK_FLAG_PARENT, DEPENDENT_DISK_FLAG_PERMANENT_LIFETIME, DEPENDENT_DISK_FLAG_READ_ONLY, DEPENDENT_DISK_FLAG_REMOTE, DEPENDENT_DISK_FLAG_REMOVABLE, DEPENDENT_DISK_FLAG_SYSTEM_VOLUME, DEPENDENT_DISK_FLAG_SYSTEM_VOLUME_PARENT, vdssys/DEPENDENT_DISK_FLAG, vdssys/DEPENDENT_DISK_FLAG_FULLY_ALLOCATED, vdssys/DEPENDENT_DISK_FLAG_MULT_BACKING_FILES, vdssys/DEPENDENT_DISK_FLAG_NONE, vdssys/DEPENDENT_DISK_FLAG_NO_DRIVE_LETTER, vdssys/DEPENDENT_DISK_FLAG_NO_HOST_DISK, vdssys/DEPENDENT_DISK_FLAG_PARENT, vdssys/DEPENDENT_DISK_FLAG_PERMANENT_LIFETIME, vdssys/DEPENDENT_DISK_FLAG_READ_ONLY, vdssys/DEPENDENT_DISK_FLAG_REMOTE, vdssys/DEPENDENT_DISK_FLAG_REMOVABLE, vdssys/DEPENDENT_DISK_FLAG_SYSTEM_VOLUME, vdssys/DEPENDENT_DISK_FLAG_SYSTEM_VOLUME_PARENT, vhd.dependent_disk_flag, virtdisk/DEPENDENT_DISK_FLAG, virtdisk/DEPENDENT_DISK_FLAG_FULLY_ALLOCATED, virtdisk/DEPENDENT_DISK_FLAG_MULT_BACKING_FILES, virtdisk/DEPENDENT_DISK_FLAG_NONE, virtdisk/DEPENDENT_DISK_FLAG_NO_DRIVE_LETTER, virtdisk/DEPENDENT_DISK_FLAG_NO_HOST_DISK, virtdisk/DEPENDENT_DISK_FLAG_PARENT, virtdisk/DEPENDENT_DISK_FLAG_PERMANENT_LIFETIME, virtdisk/DEPENDENT_DISK_FLAG_READ_ONLY, virtdisk/DEPENDENT_DISK_FLAG_REMOTE, virtdisk/DEPENDENT_DISK_FLAG_REMOVABLE, virtdisk/DEPENDENT_DISK_FLAG_SYSTEM_VOLUME, virtdisk/DEPENDENT_DISK_FLAG_SYSTEM_VOLUME_PARENT
ms.topic: enum
f1_keywords: 
 - "virtdisk/DEPENDENT_DISK_FLAG"
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
 - DEPENDENT_DISK_FLAG
product: Windows
targetos: Windows
req.typenames: DEPENDENT_DISK_FLAG
req.redist: 
ms.custom: 19H1
---

# DEPENDENT_DISK_FLAG enumeration


## -description


Contains virtual hard disk (VHD) dependency information flags.


## -enum-fields




### -field DEPENDENT_DISK_FLAG_NONE

 No flags specified. Use system defaults.


### -field DEPENDENT_DISK_FLAG_MULT_BACKING_FILES

Multiple files backing the virtual disk.


### -field DEPENDENT_DISK_FLAG_FULLY_ALLOCATED

Fully allocated virtual disk.


### -field DEPENDENT_DISK_FLAG_READ_ONLY

Read-only virtual disk.


### -field DEPENDENT_DISK_FLAG_REMOTE

 The backing file of the virtual disk is not on a local physical disk.


### -field DEPENDENT_DISK_FLAG_SYSTEM_VOLUME

 Reserved.


### -field DEPENDENT_DISK_FLAG_SYSTEM_VOLUME_PARENT

The backing file of the virtual disk is on the system volume.


### -field DEPENDENT_DISK_FLAG_REMOVABLE

The backing file of the virtual disk is on a removable physical disk.


### -field DEPENDENT_DISK_FLAG_NO_DRIVE_LETTER

Drive letters are not automatically assigned to the volumes on the virtual disk.


### -field DEPENDENT_DISK_FLAG_PARENT

The virtual disk is a parent of a differencing chain.


### -field DEPENDENT_DISK_FLAG_NO_HOST_DISK

 The virtual disk is not attached to the local host.
    For example, it is attached to a guest virtual machine.


### -field DEPENDENT_DISK_FLAG_PERMANENT_LIFETIME

The lifetime of the virtual disk is not tied to any application or process.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/VStor/virtual-storage">Virtual Storage</a>
 

 

