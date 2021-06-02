---
UID: NF:virtdisk.DeleteSnapshotVhdSet
title: DeleteSnapshotVhdSet function (virtdisk.h)
description: Deletes a snapshot from a VHD Set file.
helpviewer_keywords: ["DeleteSnapshotVhdSet","DeleteSnapshotVhdSet function [VHD]","vdssys/DeleteSnapshotVhdSet","vhd.deletesnapshotvhdset","virtdisk/DeleteSnapshotVhdSet"]
old-location: vhd\deletesnapshotvhdset.htm
tech.root: VStor
ms.assetid: F6A65E00-857A-44CF-A827-747518564DAB
ms.date: 12/05/2018
ms.keywords: DeleteSnapshotVhdSet, DeleteSnapshotVhdSet function [VHD], vdssys/DeleteSnapshotVhdSet, vhd.deletesnapshotvhdset, virtdisk/DeleteSnapshotVhdSet
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
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeleteSnapshotVhdSet
 - virtdisk/DeleteSnapshotVhdSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - DeleteSnapshotVhdSet
---

# DeleteSnapshotVhdSet function


## -description



Deletes a snapshot from a VHD Set file.

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open virtual disk. This must be a VHD Set file.

### -param Parameters [in]

A pointer to a valid <a href="/windows/win32/api/virtdisk/ns-virtdisk-delete_snapshot_vhdset_parameters">DELETE_SNAPSHOT_VHDSET_PARAMETERS</a> structure that contains snapshot deletion data.

### -param Flags [in]

Snapshot deletion flags, which must be a valid combination of the <a href="/windows/win32/api/virtdisk/ne-virtdisk-delete_snapshot_vhdset_flag">DELETE_SNAPSHOT_VHDSET_FLAG</a> enumeration.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.