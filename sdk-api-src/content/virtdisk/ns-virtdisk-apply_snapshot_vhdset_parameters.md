---
UID: NS:virtdisk._APPLY_SNAPSHOT_VHDSET_PARAMETERS
title: APPLY_SNAPSHOT_VHDSET_PARAMETERS (virtdisk.h)
description: Contains snapshot parameters, indicating information about the new snapshot to be applied.
helpviewer_keywords: ["*PAPPLY_SNAPSHOT_VHDSET_PARAMETERS","APPLY_SNAPSHOT_VHDSET_PARAMETERS","APPLY_SNAPSHOT_VHDSET_PARAMETERS structure [VHD]","PAPPLY_SNAPSHOT_VHDSET_PARAMETERS","PAPPLY_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD]","_APPLY_SNAPSHOT_VHDSET_PARAMETERS","vdssys/APPLY_SNAPSHOT_VHDSET_PARAMETERS","vdssys/PAPPLY_SNAPSHOT_VHDSET_PARAMETERS","vhd.apply_snapshot_vhdset_parameters","virtdisk/APPLY_SNAPSHOT_VHDSET_PARAMETERS","virtdisk/PAPPLY_SNAPSHOT_VHDSET_PARAMETERS"]
old-location: vhd\apply_snapshot_vhdset_parameters.htm
tech.root: VStor
ms.assetid: 0C3A8097-0630-412E-AF23-144E3D98D292
ms.date: 12/05/2018
ms.keywords: '*PAPPLY_SNAPSHOT_VHDSET_PARAMETERS, APPLY_SNAPSHOT_VHDSET_PARAMETERS, APPLY_SNAPSHOT_VHDSET_PARAMETERS structure [VHD], PAPPLY_SNAPSHOT_VHDSET_PARAMETERS, PAPPLY_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD], _APPLY_SNAPSHOT_VHDSET_PARAMETERS, vdssys/APPLY_SNAPSHOT_VHDSET_PARAMETERS, vdssys/PAPPLY_SNAPSHOT_VHDSET_PARAMETERS, vhd.apply_snapshot_vhdset_parameters, virtdisk/APPLY_SNAPSHOT_VHDSET_PARAMETERS, virtdisk/PAPPLY_SNAPSHOT_VHDSET_PARAMETERS'
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: APPLY_SNAPSHOT_VHDSET_PARAMETERS, *PAPPLY_SNAPSHOT_VHDSET_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _APPLY_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/_APPLY_SNAPSHOT_VHDSET_PARAMETERS
 - PAPPLY_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/PAPPLY_SNAPSHOT_VHDSET_PARAMETERS
 - APPLY_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/APPLY_SNAPSHOT_VHDSET_PARAMETERS
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
 - APPLY_SNAPSHOT_VHDSET_PARAMETERS
---

# APPLY_SNAPSHOT_VHDSET_PARAMETERS structure


## -description

Contains snapshot parameters, indicating information about the new snapshot to be applied.

## -struct-fields

### -field Version

An <a href="/windows/win32/api/virtdisk/ne-virtdisk-apply_snapshot_vhdset_version">APPLY_SNAPSHOT_VHDSET_VERSION</a> 
     enumeration that specifies the version of the 
     <b>APPLY_SNAPSHOT_VHDSET_PARAMETERS</b> structure being passed to or from the VHD functions.

### -field Version1

A structure with the following member.

### -field Version1.SnapshotId

The ID of the new snapshot to be applied to the VHD set.

### -field Version1.LeafSnapshotId

Indicates whether the current default leaf data should be retained as part of the apply operation. When a zero GUID is specified, the apply operation will discard the current default leaf data. When a non-zero GUID is specified, the apply operation will convert the default leaf data into a writable snapshot with the specified ID.

