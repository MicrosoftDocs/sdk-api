---
UID: NS:virtdisk._MODIFY_VHDSET_PARAMETERS
title: MODIFY_VHDSET_PARAMETERS (virtdisk.h)
description: Contains VHD Set modification parameters, indicating how the VHD Set should be altered.
helpviewer_keywords: ["*PMODIFY_VHDSET_PARAMETERS","MODIFY_VHDSET_PARAMETERS","MODIFY_VHDSET_PARAMETERS structure [VHD]","PMODIFY_VHDSET_PARAMETERS","PMODIFY_VHDSET_PARAMETERS structure pointer [VHD]","_MODIFY_VHDSET_PARAMETERS","vdssys/MODIFY_VHDSET_PARAMETERS","vdssys/PMODIFY_VHDSET_PARAMETERS","vhd.modify_vhdset_parameters","virtdisk/MODIFY_VHDSET_PARAMETERS","virtdisk/PMODIFY_VHDSET_PARAMETERS"]
old-location: vhd\modify_vhdset_parameters.htm
tech.root: VStor
ms.assetid: 558323D6-2D97-40C8-9CAF-E97604D2F742
ms.date: 12/05/2018
ms.keywords: '*PMODIFY_VHDSET_PARAMETERS, MODIFY_VHDSET_PARAMETERS, MODIFY_VHDSET_PARAMETERS structure [VHD], PMODIFY_VHDSET_PARAMETERS, PMODIFY_VHDSET_PARAMETERS structure pointer [VHD], _MODIFY_VHDSET_PARAMETERS, vdssys/MODIFY_VHDSET_PARAMETERS, vdssys/PMODIFY_VHDSET_PARAMETERS, vhd.modify_vhdset_parameters, virtdisk/MODIFY_VHDSET_PARAMETERS, virtdisk/PMODIFY_VHDSET_PARAMETERS'
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
req.typenames: MODIFY_VHDSET_PARAMETERS, *PMODIFY_VHDSET_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MODIFY_VHDSET_PARAMETERS
 - virtdisk/_MODIFY_VHDSET_PARAMETERS
 - PMODIFY_VHDSET_PARAMETERS
 - virtdisk/PMODIFY_VHDSET_PARAMETERS
 - MODIFY_VHDSET_PARAMETERS
 - virtdisk/MODIFY_VHDSET_PARAMETERS
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
 - MODIFY_VHDSET_PARAMETERS
---

# MODIFY_VHDSET_PARAMETERS structure


## -description



Contains VHD Set modification parameters, indicating how the VHD Set should be altered.

## -struct-fields

### -field Version

A value from the MODIFY_VHDSET_VERSION enumeration that determines that is the discriminant for the union.

### -field SnapshotPath

A structure with the following members.

### -field SnapshotPath.SnapshotId

The Snapshot Id in GUID format indicating which snapshot is to have its path altered in the VHD Set.

### -field SnapshotPath.SnapshotFilePath

The new file path for the Snapshot indicated by the SnapshotId field.

### -field SnapshotId

The Snapshot Id in GUID format indicating which snapshot is to be removed from the VHD Set file.

### -field DefaultFilePath

The file path for the default Snapshot of the Vhd Set.

