---
UID: NE:virtdisk._ATTACH_VIRTUAL_DISK_FLAG
title: ATTACH_VIRTUAL_DISK_FLAG (virtdisk.h)
description: Contains virtual disk attach request flags.
helpviewer_keywords: ["ATTACH_VIRTUAL_DISK_FLAG","ATTACH_VIRTUAL_DISK_FLAG enumeration [VHD]","ATTACH_VIRTUAL_DISK_FLAG_NONE","ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER","ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST","ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME","ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY","vdssys/ATTACH_VIRTUAL_DISK_FLAG","vdssys/ATTACH_VIRTUAL_DISK_FLAG_NONE","vdssys/ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER","vdssys/ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST","vdssys/ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME","vdssys/ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY","vhd.attach_virtual_disk_flag","vhd.surface_virtual_disk_flag","virtdisk/ATTACH_VIRTUAL_DISK_FLAG","virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NONE","virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER","virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST","virtdisk/ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME","virtdisk/ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY"]
old-location: vhd\attach_virtual_disk_flag.htm
tech.root: VStor
ms.assetid: 5792c2e2-0598-43ff-8c0f-5fb4a1a37656
ms.date: 12/05/2018
ms.keywords: ATTACH_VIRTUAL_DISK_FLAG, ATTACH_VIRTUAL_DISK_FLAG enumeration [VHD], ATTACH_VIRTUAL_DISK_FLAG_NONE, ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER, ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST, ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME, ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY, vdssys/ATTACH_VIRTUAL_DISK_FLAG, vdssys/ATTACH_VIRTUAL_DISK_FLAG_NONE, vdssys/ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER, vdssys/ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST, vdssys/ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME, vdssys/ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY, vhd.attach_virtual_disk_flag, vhd.surface_virtual_disk_flag, virtdisk/ATTACH_VIRTUAL_DISK_FLAG, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NONE, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME, virtdisk/ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY
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
req.typenames: ATTACH_VIRTUAL_DISK_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ATTACH_VIRTUAL_DISK_FLAG
 - virtdisk/_ATTACH_VIRTUAL_DISK_FLAG
 - ATTACH_VIRTUAL_DISK_FLAG
 - virtdisk/ATTACH_VIRTUAL_DISK_FLAG
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
 - ATTACH_VIRTUAL_DISK_FLAG
---

# ATTACH_VIRTUAL_DISK_FLAG enumeration


## -description

Contains virtual disk attach request flags.

## -enum-fields

### -field ATTACH_VIRTUAL_DISK_FLAG_NONE:0x00000000

No flags. Use system defaults.

This enumeration value is not supported for ISO virtual disks. 
       <b>ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY</b> must be specified.

### -field ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY:0x00000001

Attach the virtual disk as read-only.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER:0x00000002

No drive letters are assigned to the disk's volumes.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME:0x00000004

Will decouple the virtual disk lifetime from that of the <i>VirtualDiskHandle</i>. The 
       virtual disk will be attached until the 
       <a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk">DetachVirtualDisk</a> function is called, even if all 
       open handles to the virtual disk are closed.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST:0x00000008

Reserved.

This flag is not supported for ISO virtual disks.

### -field ATTACH_VIRTUAL_DISK_FLAG_NO_SECURITY_DESCRIPTOR:0x00000010

### -field ATTACH_VIRTUAL_DISK_FLAG_BYPASS_DEFAULT_ENCRYPTION_POLICY:0x00000020

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
