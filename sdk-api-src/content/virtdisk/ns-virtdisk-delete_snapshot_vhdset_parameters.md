---
UID: NS:virtdisk._DELETE_SNAPSHOT_VHDSET_PARAMETERS
title: DELETE_SNAPSHOT_VHDSET_PARAMETERS (virtdisk.h)
description: Contains snapshot deletion parameters, designating which snapshot to delete from the VHD Set.
helpviewer_keywords: ["*PDELETE_SNAPSHOT_VHDSET_PARAMETERS","DELETE_SNAPSHOT_VHDSET_PARAMETERS","DELETE_SNAPSHOT_VHDSET_PARAMETERS structure [VHD]","PDELETE_SNAPSHOT_VHDSET_PARAMETERS","PDELETE_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD]","_DELETE_SNAPSHOT_VHDSET_PARAMETERS","vdssys/DELETE_SNAPSHOT_VHDSET_PARAMETERS","vdssys/PDELETE_SNAPSHOT_VHDSET_PARAMETERS","vhd.delete_snapshot_vhdset_parameters","virtdisk/DELETE_SNAPSHOT_VHDSET_PARAMETERS","virtdisk/PDELETE_SNAPSHOT_VHDSET_PARAMETERS"]
old-location: vhd\delete_snapshot_vhdset_parameters.htm
tech.root: VStor
ms.assetid: A10EB006-2FE5-4445-9E2F-DF2C1AF0A44F
ms.date: 12/05/2018
ms.keywords: '*PDELETE_SNAPSHOT_VHDSET_PARAMETERS, DELETE_SNAPSHOT_VHDSET_PARAMETERS, DELETE_SNAPSHOT_VHDSET_PARAMETERS structure [VHD], PDELETE_SNAPSHOT_VHDSET_PARAMETERS, PDELETE_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD], _DELETE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/DELETE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/PDELETE_SNAPSHOT_VHDSET_PARAMETERS, vhd.delete_snapshot_vhdset_parameters, virtdisk/DELETE_SNAPSHOT_VHDSET_PARAMETERS, virtdisk/PDELETE_SNAPSHOT_VHDSET_PARAMETERS'
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
req.typenames: DELETE_SNAPSHOT_VHDSET_PARAMETERS, *PDELETE_SNAPSHOT_VHDSET_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DELETE_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/_DELETE_SNAPSHOT_VHDSET_PARAMETERS
 - PDELETE_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/PDELETE_SNAPSHOT_VHDSET_PARAMETERS
 - DELETE_SNAPSHOT_VHDSET_PARAMETERS
 - virtdisk/DELETE_SNAPSHOT_VHDSET_PARAMETERS
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
 - DELETE_SNAPSHOT_VHDSET_PARAMETERS
---

# DELETE_SNAPSHOT_VHDSET_PARAMETERS structure


## -description



Contains snapshot deletion parameters, designating which snapshot to delete from the VHD Set.

## -struct-fields

### -field Version

A value from the <a href="/windows/win32/api/virtdisk/ne-virtdisk-delete_snapshot_vhdset_version">DELETE_SNAPSHOT_VHDSET_VERSION</a> enumeration that is the discriminant for the union.

### -field Version1

A structure with the following member.

### -field Version1.SnapshotId

The Snapshot Id in GUID format indicating which snapshot is to be deleted from the VHD Set.

