---
UID: NE:virtdisk._ATTACH_VIRTUAL_DISK_FLAG
title: "_ATTACH_VIRTUAL_DISK_FLAG"
author: windows-sdk-content
description: Contains virtual disk attach request flags.
old-location: vhd\attach_virtual_disk_flag.htm
tech.root: VStor
ms.assetid: 5792c2e2-0598-43ff-8c0f-5fb4a1a37656
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ATTACH_VIRTUAL_DISK_FLAG, ATTACH_VIRTUAL_DISK_FLAG enumeration [VHD], ATTACH_VIRTUAL_DISK_FLAG_NONE, ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER, ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST, ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME, ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY, _ATTACH_VIRTUAL_DISK_FLAG, vdssys/ATTACH_VIRTUAL_DISK_FLAG, vdssys/ATTACH_VIRTUAL_DISK_FLAG_NONE, vdssys/ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER, vdssys/ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST, vdssys/ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME, vdssys/ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY, vhd.attach_virtual_disk_flag, vhd.surface_virtual_disk_flag, virtdisk/ATTACH_VIRTUAL_DISK_FLAG, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NONE, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY
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
 - ATTACH_VIRTUAL_DISK_FLAG
product: Windows
targetos: Windows
req.typenames: ATTACH_VIRTUAL_DISK_FLAG
req.redist: 
---

# _ATTACH_VIRTUAL_DISK_FLAG enumeration


## -description


Contains virtual disk attach request flags.


## -enum-fields




### -field ATTACH_VIRTUAL_DISK_FLAG_NONE

No flags. Use system defaults.

This enumeration value is not supported for ISO virtual disks. 
       <b>ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY</b> must be specified.


### -field ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY

Attach the virtual disk as read-only.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER

No drive letters are assigned to the disk's volumes.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME

Will decouple the virtual disk lifetime from that of the <i>VirtualDiskHandle</i>. The 
       virtual disk will be attached until the 
       <a href="https://msdn.microsoft.com/9b3874e1-e107-42f8-9ede-eb1eb6164ed2">DetachVirtualDisk</a> function is called, even if all 
       open handles to the virtual disk are closed.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST

Reserved.

This flag is not supported for ISO virtual disks.


### -field ATTACH_VIRTUAL_DISK_FLAG_NO_SECURITY_DESCRIPTOR


### -field ATTACH_VIRTUAL_DISK_FLAG_BYPASS_DEFAULT_ENCRYPTION_POLICY




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

