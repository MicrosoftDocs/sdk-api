---
UID: NE:virtdisk._OPEN_VIRTUAL_DISK_FLAG
title: OPEN_VIRTUAL_DISK_FLAG (virtdisk.h)
author: windows-sdk-content
description: Contains virtual hard disk (VHD) or CD or DVD image file (ISO) open request flags.
old-location: vhd\open_virtual_disk_flag.htm
tech.root: VStor
ms.assetid: edc7d3ad-23a0-4e7a-82d5-8ac4df785f35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OPEN_VIRTUAL_DISK_FLAG, OPEN_VIRTUAL_DISK_FLAG enumeration [VHD], OPEN_VIRTUAL_DISK_FLAG_BLANK_FILE, OPEN_VIRTUAL_DISK_FLAG_BOOT_DRIVE, OPEN_VIRTUAL_DISK_FLAG_CACHED_IO, OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN, OPEN_VIRTUAL_DISK_FLAG_NONE, OPEN_VIRTUAL_DISK_FLAG_NO_PARENTS, vdssys/OPEN_VIRTUAL_DISK_FLAG, vdssys/OPEN_VIRTUAL_DISK_FLAG_BLANK_FILE, vdssys/OPEN_VIRTUAL_DISK_FLAG_BOOT_DRIVE, vdssys/OPEN_VIRTUAL_DISK_FLAG_CACHED_IO, vdssys/OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN, vdssys/OPEN_VIRTUAL_DISK_FLAG_NONE, vdssys/OPEN_VIRTUAL_DISK_FLAG_NO_PARENTS, vhd.open_virtual_disk_flag, virtdisk/OPEN_VIRTUAL_DISK_FLAG, virtdisk/OPEN_VIRTUAL_DISK_FLAG_BLANK_FILE, virtdisk/OPEN_VIRTUAL_DISK_FLAG_BOOT_DRIVE, virtdisk/OPEN_VIRTUAL_DISK_FLAG_CACHED_IO, virtdisk/OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN, virtdisk/OPEN_VIRTUAL_DISK_FLAG_NONE, virtdisk/OPEN_VIRTUAL_DISK_FLAG_NO_PARENTS
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
 - OPEN_VIRTUAL_DISK_FLAG
product: Windows
targetos: Windows
req.typenames: OPEN_VIRTUAL_DISK_FLAG
req.redist: 
ms.custom: 19H1
---

# OPEN_VIRTUAL_DISK_FLAG enumeration


## -description


Contains virtual hard disk (VHD) or CD or DVD image file (ISO) open request flags.


## -enum-fields




### -field OPEN_VIRTUAL_DISK_FLAG_NONE

No flag specified.


### -field OPEN_VIRTUAL_DISK_FLAG_NO_PARENTS

Open the VHD file (backing store) without opening any differencing-chain parents. Used to correct broken 
       parent links.

This flag is not supported for ISO virtual disks.


### -field OPEN_VIRTUAL_DISK_FLAG_BLANK_FILE

Reserved.

This flag is not supported for ISO virtual disks.


### -field OPEN_VIRTUAL_DISK_FLAG_BOOT_DRIVE

Reserved.

This flag is not supported for ISO virtual disks.


### -field OPEN_VIRTUAL_DISK_FLAG_CACHED_IO

Indicates that the virtual disk should be opened in cached mode. By default the virtual disks are opened 
       using <b>FILE_FLAG_NO_BUFFERING</b> and 
       <b>FILE_FLAG_WRITE_THROUGH</b>.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN

Indicates the VHD file is to be opened without opening any differencing-chain parents and the parent chain is 
       to be created manually using the 
       <a href="https://docs.microsoft.com/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent">AddVirtualDiskParent</a> function.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field OPEN_VIRTUAL_DISK_FLAG_PARENT_CACHED_IO


### -field OPEN_VIRTUAL_DISK_FLAG_VHDSET_FILE_ONLY


### -field OPEN_VIRTUAL_DISK_FLAG_IGNORE_RELATIVE_PARENT_LOCATOR


### -field OPEN_VIRTUAL_DISK_FLAG_NO_WRITE_HARDENING




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
 

 

