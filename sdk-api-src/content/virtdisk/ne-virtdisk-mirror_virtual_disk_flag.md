---
UID: NE:virtdisk._MIRROR_VIRTUAL_DISK_FLAG
title: MIRROR_VIRTUAL_DISK_FLAG (virtdisk.h)
description: Contains virtual hard disk (VHD) mirror request flags.
helpviewer_keywords: ["MIRROR_VIRTUAL_DISK_FLAG","MIRROR_VIRTUAL_DISK_FLAG enumeration [VHD]","MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE","MIRROR_VIRTUAL_DISK_FLAG_NONE","vdssys/MIRROR_VIRTUAL_DISK_FLAG","vdssys/MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE","vdssys/MIRROR_VIRTUAL_DISK_FLAG_NONE","vhd.mirror_virtual_disk_flag","virtdisk/MIRROR_VIRTUAL_DISK_FLAG","virtdisk/MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE","virtdisk/MIRROR_VIRTUAL_DISK_FLAG_NONE"]
old-location: vhd\mirror_virtual_disk_flag.htm
tech.root: VStor
ms.assetid: 14051691-eacb-40b8-a8ae-822bc054d0a1
ms.date: 12/05/2018
ms.keywords: MIRROR_VIRTUAL_DISK_FLAG, MIRROR_VIRTUAL_DISK_FLAG enumeration [VHD], MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE, MIRROR_VIRTUAL_DISK_FLAG_NONE, vdssys/MIRROR_VIRTUAL_DISK_FLAG, vdssys/MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE, vdssys/MIRROR_VIRTUAL_DISK_FLAG_NONE, vhd.mirror_virtual_disk_flag, virtdisk/MIRROR_VIRTUAL_DISK_FLAG, virtdisk/MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE, virtdisk/MIRROR_VIRTUAL_DISK_FLAG_NONE
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MIRROR_VIRTUAL_DISK_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIRROR_VIRTUAL_DISK_FLAG
 - virtdisk/_MIRROR_VIRTUAL_DISK_FLAG
 - MIRROR_VIRTUAL_DISK_FLAG
 - virtdisk/MIRROR_VIRTUAL_DISK_FLAG
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
 - MIRROR_VIRTUAL_DISK_FLAG
---

# MIRROR_VIRTUAL_DISK_FLAG enumeration


## -description

Contains virtual hard disk (VHD) mirror request flags.

## -enum-fields

### -field MIRROR_VIRTUAL_DISK_FLAG_NONE:0x00000000

The mirror virtual disk file does not exist, and needs to be created.

### -field MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE:0x00000001

Create the mirror using an existing file.

### -field MIRROR_VIRTUAL_DISK_FLAG_SKIP_MIRROR_ACTIVATION:0x00000002

## -see-also

<a href="/windows/win32/api/virtdisk/ns-virtdisk-mirror_virtual_disk_parameters">MIRROR_VIRTUAL_DISK_PARAMETERS</a>



<a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk">MirrorVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323698(v=vs.85)">VHD Enumerations</a>
