---
UID: NE:virtdisk._MIRROR_VIRTUAL_DISK_VERSION
title: MIRROR_VIRTUAL_DISK_VERSION (virtdisk.h)
description: Contains the version of the virtual disk MIRROR_VIRTUAL_DISK_PARAMETERS structure used by the MirrorVirtualDisk function.
helpviewer_keywords: ["MIRROR_VIRTUAL_DISK_VERSION","MIRROR_VIRTUAL_DISK_VERSION enumeration [VHD]","MIRROR_VIRTUAL_DISK_VERSION_1","MIRROR_VIRTUAL_DISK_VERSION_UNSPECIFIED","vdssys/MIRROR_VIRTUAL_DISK_VERSION","vdssys/MIRROR_VIRTUAL_DISK_VERSION_1","vdssys/MIRROR_VIRTUAL_DISK_VERSION_UNSPECIFIED","vhd.mirror_virtual_disk_version","virtdisk/MIRROR_VIRTUAL_DISK_VERSION","virtdisk/MIRROR_VIRTUAL_DISK_VERSION_1","virtdisk/MIRROR_VIRTUAL_DISK_VERSION_UNSPECIFIED"]
old-location: vhd\mirror_virtual_disk_version.htm
tech.root: VStor
ms.assetid: 42045e2b-3e3b-4497-b6bb-18f360139c18
ms.date: 12/05/2018
ms.keywords: MIRROR_VIRTUAL_DISK_VERSION, MIRROR_VIRTUAL_DISK_VERSION enumeration [VHD], MIRROR_VIRTUAL_DISK_VERSION_1, MIRROR_VIRTUAL_DISK_VERSION_UNSPECIFIED, vdssys/MIRROR_VIRTUAL_DISK_VERSION, vdssys/MIRROR_VIRTUAL_DISK_VERSION_1, vdssys/MIRROR_VIRTUAL_DISK_VERSION_UNSPECIFIED, vhd.mirror_virtual_disk_version, virtdisk/MIRROR_VIRTUAL_DISK_VERSION, virtdisk/MIRROR_VIRTUAL_DISK_VERSION_1, virtdisk/MIRROR_VIRTUAL_DISK_VERSION_UNSPECIFIED
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
req.typenames: MIRROR_VIRTUAL_DISK_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIRROR_VIRTUAL_DISK_VERSION
 - virtdisk/_MIRROR_VIRTUAL_DISK_VERSION
 - MIRROR_VIRTUAL_DISK_VERSION
 - virtdisk/MIRROR_VIRTUAL_DISK_VERSION
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
 - MIRROR_VIRTUAL_DISK_VERSION
---

# MIRROR_VIRTUAL_DISK_VERSION enumeration


## -description

Contains the version of the virtual disk 
     <a href="/windows/win32/api/virtdisk/ns-virtdisk-mirror_virtual_disk_parameters">MIRROR_VIRTUAL_DISK_PARAMETERS</a> structure 
     used by the <a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk">MirrorVirtualDisk</a> 
     function.

## -enum-fields

### -field MIRROR_VIRTUAL_DISK_VERSION_UNSPECIFIED:0

Unsupported.

### -field MIRROR_VIRTUAL_DISK_VERSION_1:1

Use the <b>Version1</b> member.

## -see-also

<a href="/windows/win32/api/virtdisk/ns-virtdisk-mirror_virtual_disk_parameters">MIRROR_VIRTUAL_DISK_PARAMETERS</a>



<a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk">MirrorVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323698(v=vs.85)">VHD Enumerations</a>
