---
UID: NS:virtdisk._TAKE_SNAPSHOT_VHDSET_PARAMETERS
title: TAKE_SNAPSHOT_VHDSET_PARAMETERS (virtdisk.h)
description: Contains snapshot parameters, indicating information about the new snapshot to be created.
helpviewer_keywords: ["*PTAKE_SNAPSHOT_VHDSET_PARAMETERS","PTAKE_SNAPSHOT_VHDSET_PARAMETERS","PTAKE_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD]","TAKE_SNAPSHOT_VHDSET_PARAMETERS","TAKE_SNAPSHOT_VHDSET_PARAMETERS structure [VHD]","_TAKE_SNAPSHOT_VHDSET_PARAMETERS","vdssys/PTAKE_SNAPSHOT_VHDSET_PARAMETERS","vdssys/TAKE_SNAPSHOT_VHDSET_PARAMETERS","vhd.take_snapshot_vhdset_parameters","virtdisk/PTAKE_SNAPSHOT_VHDSET_PARAMETERS","virtdisk/TAKE_SNAPSHOT_VHDSET_PARAMETERS"]
old-location: vhd\take_snapshot_vhdset_parameters.htm
tech.root: VStor
ms.assetid: 39D7287B-FA5E-4584-8E0A-69A857736D02
ms.date: 12/05/2018
ms.keywords: '*PTAKE_SNAPSHOT_VHDSET_PARAMETERS, PTAKE_SNAPSHOT_VHDSET_PARAMETERS, PTAKE_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD], TAKE_SNAPSHOT_VHDSET_PARAMETERS, TAKE_SNAPSHOT_VHDSET_PARAMETERS structure [VHD], _TAKE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/PTAKE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/TAKE_SNAPSHOT_VHDSET_PARAMETERS, vhd.take_snapshot_vhdset_parameters, virtdisk/PTAKE_SNAPSHOT_VHDSET_PARAMETERS, virtdisk/TAKE_SNAPSHOT_VHDSET_PARAMETERS'
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
req.typenames: TAKE_SNAPSHOT_VHDSET_PARAMETERS, *PTAKE_SNAPSHOT_VHDSET_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAKE_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/_TAKE_SNAPSHOT_VHDSET_PARAMETERS
 - PTAKE_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/PTAKE_SNAPSHOT_VHDSET_PARAMETERS
 - TAKE_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/TAKE_SNAPSHOT_VHDSET_PARAMETERS
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
 - TAKE_SNAPSHOT_VHDSET_PARAMETERS
---

# TAKE_SNAPSHOT_VHDSET_PARAMETERS structure


## -description



Contains snapshot parameters, indicating information about the new snapshot to be created.

## -struct-fields

### -field Version

A value from the <a href="/windows/win32/api/virtdisk/ne-virtdisk-take_snapshot_vhdset_version">TAKE_SNAPSHOT_VHDSET_VERSION</a> enumeration that is the discriminant for the union.

### -field Version1

A structure with the following member.

### -field Version1.SnapshotId

The Id of the new Snapshot to be added to the Vhd Set.

