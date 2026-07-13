---
UID: NE:virtdisk._OPEN_VIRTUAL_DISK_VERSION
title: OPEN_VIRTUAL_DISK_VERSION (virtdisk.h)
description: Contains the version of the virtual disk OPEN_VIRTUAL_DISK_PARAMETERS structure to use in calls to virtual disk functions.
helpviewer_keywords: ["OPEN_VIRTUAL_DISK_VERSION","OPEN_VIRTUAL_DISK_VERSION enumeration [VHD]","OPEN_VIRTUAL_DISK_VERSION_1","OPEN_VIRTUAL_DISK_VERSION_2","OPEN_VIRTUAL_DISK_VERSION_UNSPECIFIED","vdssys/OPEN_VIRTUAL_DISK_VERSION","vdssys/OPEN_VIRTUAL_DISK_VERSION_1","vdssys/OPEN_VIRTUAL_DISK_VERSION_2","vdssys/OPEN_VIRTUAL_DISK_VERSION_UNSPECIFIED","vhd.open_virtual_disk_version","virtdisk/OPEN_VIRTUAL_DISK_VERSION","virtdisk/OPEN_VIRTUAL_DISK_VERSION_1","virtdisk/OPEN_VIRTUAL_DISK_VERSION_2","virtdisk/OPEN_VIRTUAL_DISK_VERSION_UNSPECIFIED"]
old-location: vhd\open_virtual_disk_version.htm
tech.root: VStor
ms.assetid: 3f45324a-6e31-43d6-9fc9-65c85e6c3493
ms.date: 12/05/2018
ms.keywords: OPEN_VIRTUAL_DISK_VERSION, OPEN_VIRTUAL_DISK_VERSION enumeration [VHD], OPEN_VIRTUAL_DISK_VERSION_1, OPEN_VIRTUAL_DISK_VERSION_2, OPEN_VIRTUAL_DISK_VERSION_UNSPECIFIED, vdssys/OPEN_VIRTUAL_DISK_VERSION, vdssys/OPEN_VIRTUAL_DISK_VERSION_1, vdssys/OPEN_VIRTUAL_DISK_VERSION_2, vdssys/OPEN_VIRTUAL_DISK_VERSION_UNSPECIFIED, vhd.open_virtual_disk_version, virtdisk/OPEN_VIRTUAL_DISK_VERSION, virtdisk/OPEN_VIRTUAL_DISK_VERSION_1, virtdisk/OPEN_VIRTUAL_DISK_VERSION_2, virtdisk/OPEN_VIRTUAL_DISK_VERSION_UNSPECIFIED
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
req.typenames: OPEN_VIRTUAL_DISK_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPEN_VIRTUAL_DISK_VERSION
 - virtdisk/_OPEN_VIRTUAL_DISK_VERSION
 - OPEN_VIRTUAL_DISK_VERSION
 - virtdisk/OPEN_VIRTUAL_DISK_VERSION
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
 - OPEN_VIRTUAL_DISK_VERSION
---

# OPEN_VIRTUAL_DISK_VERSION enumeration


## -description

Contains the version of the virtual disk 
    <a href="/windows/win32/api/virtdisk/ns-virtdisk-open_virtual_disk_parameters">OPEN_VIRTUAL_DISK_PARAMETERS</a> structure to 
    use in calls to virtual disk functions.

## -enum-fields

### -field OPEN_VIRTUAL_DISK_VERSION_UNSPECIFIED:0

Not supported.

### -field OPEN_VIRTUAL_DISK_VERSION_1:1

The <b>Version1</b> member structure will be used.

### -field OPEN_VIRTUAL_DISK_VERSION_2:2

The <b>Version2</b> member structure will be used.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported until Windows 8 and Windows Server 2012.

### -field OPEN_VIRTUAL_DISK_VERSION_3:3

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
