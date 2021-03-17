---
UID: NS:virtdisk._COMPACT_VIRTUAL_DISK_PARAMETERS
title: COMPACT_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains virtual hard disk (VHD) compacting parameters.
helpviewer_keywords: ["*PCOMPACT_VIRTUAL_DISK_PARAMETERS","COMPACT_VIRTUAL_DISK_PARAMETERS","COMPACT_VIRTUAL_DISK_PARAMETERS structure [VHD]","PCOMPACT_VIRTUAL_DISK_PARAMETERS","PCOMPACT_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","_COMPACT_VIRTUAL_DISK_PARAMETERS","vdssys/COMPACT_VIRTUAL_DISK_PARAMETERS","vdssys/PCOMPACT_VIRTUAL_DISK_PARAMETERS","vhd.compact_virtual_disk_parameters","virtdisk/COMPACT_VIRTUAL_DISK_PARAMETERS","virtdisk/PCOMPACT_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\compact_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 3e58101c-c8a9-432e-99c4-9e418a887b9e
ms.date: 12/05/2018
ms.keywords: '*PCOMPACT_VIRTUAL_DISK_PARAMETERS, COMPACT_VIRTUAL_DISK_PARAMETERS, COMPACT_VIRTUAL_DISK_PARAMETERS structure [VHD], PCOMPACT_VIRTUAL_DISK_PARAMETERS, PCOMPACT_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _COMPACT_VIRTUAL_DISK_PARAMETERS, vdssys/COMPACT_VIRTUAL_DISK_PARAMETERS, vdssys/PCOMPACT_VIRTUAL_DISK_PARAMETERS, vhd.compact_virtual_disk_parameters, virtdisk/COMPACT_VIRTUAL_DISK_PARAMETERS, virtdisk/PCOMPACT_VIRTUAL_DISK_PARAMETERS'
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
req.typenames: COMPACT_VIRTUAL_DISK_PARAMETERS, *PCOMPACT_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COMPACT_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_COMPACT_VIRTUAL_DISK_PARAMETERS
 - PCOMPACT_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PCOMPACT_VIRTUAL_DISK_PARAMETERS
 - COMPACT_VIRTUAL_DISK_PARAMETERS
 - virtdisk/COMPACT_VIRTUAL_DISK_PARAMETERS
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
 - COMPACT_VIRTUAL_DISK_PARAMETERS
---

# COMPACT_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains virtual hard disk (VHD)  compacting parameters.

## -struct-fields

### -field Version

A <a href="/windows/win32/api/virtdisk/ne-virtdisk-compact_virtual_disk_version">COMPACT_VIRTUAL_DISK_VERSION</a> 
     enumeration that specifies the version of the 
     <b>COMPACT_VIRTUAL_DISK_PARAMETERS</b> 
     structure being passed to or from the VHD functions.

### -field Version1

A structure with the following member.

### -field Version1.Reserved

Reserved. Must be set to zero.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>