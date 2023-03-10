---
UID: NF:virtdisk.TakeSnapshotVhdSet
title: TakeSnapshotVhdSet function (virtdisk.h)
description: Creates a snapshot of the current virtual disk for VHD Set files.
helpviewer_keywords: ["TakeSnapshotVhdSet","TakeSnapshotVhdSet function [VHD]","vdssys/TakeSnapshotVhdSet","vhd.takesnapshotvhdset","virtdisk/TakeSnapshotVhdSet"]
old-location: vhd\takesnapshotvhdset.htm
tech.root: VStor
ms.assetid: 370C6DB2-EA0F-4B6F-BA14-CE14377E2314
ms.date: 12/05/2018
ms.keywords: TakeSnapshotVhdSet, TakeSnapshotVhdSet function [VHD], vdssys/TakeSnapshotVhdSet, vhd.takesnapshotvhdset, virtdisk/TakeSnapshotVhdSet
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
 - TakeSnapshotVhdSet
 - virtdisk/TakeSnapshotVhdSet
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
 - TakeSnapshotVhdSet
---

# TakeSnapshotVhdSet function


## -description



Creates a snapshot of the current virtual disk for VHD Set files.

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open virtual disk. This must be a VHD Set file.

### -param Parameters [in]

A pointer to a valid <a href="/windows/win32/api/virtdisk/ns-virtdisk-take_snapshot_vhdset_parameters">TAKE_SNAPSHOT_VHDSET_PARAMETERS</a> structure that contains snapshot data.

### -param Flags [in]

Snapshot flags, which must be a valid combination of the <a href="/windows/win32/api/virtdisk/ne-virtdisk-take_snapshot_vhdset_flag">TAKE_SNAPSHOT_VHDSET_FLAG</a> enumeration

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.