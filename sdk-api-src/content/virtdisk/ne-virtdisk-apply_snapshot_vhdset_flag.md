---
UID: NE:virtdisk._APPLY_SNAPSHOT_VHDSET_FLAG
title: APPLY_SNAPSHOT_VHDSET_FLAG (virtdisk.h)

description: Contains flags affecting the behavior of the ApplySnapshotVhdSet function.
old-location: vhd\apply_snapshot_vhdset_flag.htm
tech.root: VStor
ms.assetid: 96ED6EB4-BB11-430D-9B2E-C905C223D261

ms.date: 12/05/2018
ms.keywords: "*PAPPLY_SNAPSHOT_VHDSET_FLAG, APPLY_SNAPSHOT_VHDSET_FLAG, APPLY_SNAPSHOT_VHDSET_FLAG enumeration [VHD], APPLY_SNAPSHOT_VHDSET_FLAG_NONE, APPLY_SNAPSHOT_VHDSET_FLAG_WRITEABLE, PAPPLY_SNAPSHOT_VHDSET_FLAG, PAPPLY_SNAPSHOT_VHDSET_FLAG enumeration pointer [VHD], vdssys/APPLY_SNAPSHOT_VHDSET_FLAG, vdssys/APPLY_SNAPSHOT_VHDSET_FLAG_NONE, vdssys/APPLY_SNAPSHOT_VHDSET_FLAG_WRITEABLE, vdssys/PAPPLY_SNAPSHOT_VHDSET_FLAG, vhd.apply_snapshot_vhdset_flag, virtdisk/APPLY_SNAPSHOT_VHDSET_FLAG, virtdisk/APPLY_SNAPSHOT_VHDSET_FLAG_NONE, virtdisk/APPLY_SNAPSHOT_VHDSET_FLAG_WRITEABLE, virtdisk/PAPPLY_SNAPSHOT_VHDSET_FLAG"
ms.topic: enum
f1_keywords: 
 - "virtdisk/APPLY_SNAPSHOT_VHDSET_FLAG"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - APPLY_SNAPSHOT_VHDSET_FLAG
targetos: Windows
req.typenames: APPLY_SNAPSHOT_VHDSET_FLAG, *PAPPLY_SNAPSHOT_VHDSET_FLAG
req.redist: 
ms.custom: 19H1
---

# APPLY_SNAPSHOT_VHDSET_FLAG enumeration


## -description


Contains flags affecting the behavior of the <a href="https://docs.microsoft.com/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset">ApplySnapshotVhdSet</a> function.


## -enum-fields




### -field APPLY_SNAPSHOT_VHDSET_FLAG_NONE

No flag specified.


### -field APPLY_SNAPSHOT_VHDSET_FLAG_WRITEABLE

Indicates that the snapshot to be applied was created as a writeable snapshot type. 


