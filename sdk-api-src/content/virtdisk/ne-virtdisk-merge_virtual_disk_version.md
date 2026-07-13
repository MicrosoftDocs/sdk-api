---
UID: NE:virtdisk._MERGE_VIRTUAL_DISK_VERSION
title: MERGE_VIRTUAL_DISK_VERSION (virtdisk.h)
description: Contains the version of the virtual hard disk (VHD) MERGE_VIRTUAL_DISK_PARAMETERS structure to use in calls to VHD functions.
helpviewer_keywords: ["MERGE_VIRTUAL_DISK_VERSION","MERGE_VIRTUAL_DISK_VERSION enumeration [VHD]","MERGE_VIRTUAL_DISK_VERSION_1","MERGE_VIRTUAL_DISK_VERSION_2","MERGE_VIRTUAL_DISK_VERSION_UNSPECIFIED","vdssys/MERGE_VIRTUAL_DISK_VERSION","vdssys/MERGE_VIRTUAL_DISK_VERSION_1","vdssys/MERGE_VIRTUAL_DISK_VERSION_2","vdssys/MERGE_VIRTUAL_DISK_VERSION_UNSPECIFIED","vhd.merge_virtual_disk_version","virtdisk/MERGE_VIRTUAL_DISK_VERSION","virtdisk/MERGE_VIRTUAL_DISK_VERSION_1","virtdisk/MERGE_VIRTUAL_DISK_VERSION_2","virtdisk/MERGE_VIRTUAL_DISK_VERSION_UNSPECIFIED"]
old-location: vhd\merge_virtual_disk_version.htm
tech.root: VStor
ms.assetid: 1f542a51-d314-4add-a389-d450785b0a73
ms.date: 12/05/2018
ms.keywords: MERGE_VIRTUAL_DISK_VERSION, MERGE_VIRTUAL_DISK_VERSION enumeration [VHD], MERGE_VIRTUAL_DISK_VERSION_1, MERGE_VIRTUAL_DISK_VERSION_2, MERGE_VIRTUAL_DISK_VERSION_UNSPECIFIED, vdssys/MERGE_VIRTUAL_DISK_VERSION, vdssys/MERGE_VIRTUAL_DISK_VERSION_1, vdssys/MERGE_VIRTUAL_DISK_VERSION_2, vdssys/MERGE_VIRTUAL_DISK_VERSION_UNSPECIFIED, vhd.merge_virtual_disk_version, virtdisk/MERGE_VIRTUAL_DISK_VERSION, virtdisk/MERGE_VIRTUAL_DISK_VERSION_1, virtdisk/MERGE_VIRTUAL_DISK_VERSION_2, virtdisk/MERGE_VIRTUAL_DISK_VERSION_UNSPECIFIED
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
req.typenames: MERGE_VIRTUAL_DISK_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MERGE_VIRTUAL_DISK_VERSION
 - virtdisk/_MERGE_VIRTUAL_DISK_VERSION
 - MERGE_VIRTUAL_DISK_VERSION
 - virtdisk/MERGE_VIRTUAL_DISK_VERSION
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
 - MERGE_VIRTUAL_DISK_VERSION
---

# MERGE_VIRTUAL_DISK_VERSION enumeration


## -description

Contains the version of the virtual hard disk (VHD) 
    <a href="/windows/win32/api/virtdisk/ns-virtdisk-merge_virtual_disk_parameters">MERGE_VIRTUAL_DISK_PARAMETERS</a> structure to 
    use in calls to VHD functions.

## -enum-fields

### -field MERGE_VIRTUAL_DISK_VERSION_UNSPECIFIED:0

Not supported.

### -field MERGE_VIRTUAL_DISK_VERSION_1:1

The <b>Version1</b> member structure will be used.

### -field MERGE_VIRTUAL_DISK_VERSION_2:2

The <b>Version2</b> member structure will be used.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported until Windows 8 and Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
