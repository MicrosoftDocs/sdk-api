---
UID: NF:virtdisk.MergeVirtualDisk
title: MergeVirtualDisk function (virtdisk.h)
description: Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.
helpviewer_keywords: ["MergeVirtualDisk","MergeVirtualDisk function [VHD]","vdssys/MergeVirtualDisk","vhd.mergevirtualdisk","virtdisk/MergeVirtualDisk"]
old-location: vhd\mergevirtualdisk.htm
tech.root: VStor
ms.assetid: 9a9068d1-2f81-42a2-a3b2-6030a24a4445
ms.date: 12/05/2018
ms.keywords: MergeVirtualDisk, MergeVirtualDisk function [VHD], vdssys/MergeVirtualDisk, vhd.mergevirtualdisk, virtdisk/MergeVirtualDisk
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
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MergeVirtualDisk
 - virtdisk/MergeVirtualDisk
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
 - MergeVirtualDisk
---

# MergeVirtualDisk function


## -description

Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag. For information on how to open a virtual disk, see the <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function.

### -param Flags [in]

Must be the <b>MERGE_VIRTUAL_DISK_FLAG_NONE</b> value of the <a href="/windows/win32/api/virtdisk/ne-virtdisk-merge_virtual_disk_flag">MERGE_VIRTUAL_DISK_FLAG</a> enumeration.

### -param Parameters [in]

A pointer to a valid <a href="/windows/win32/api/virtdisk/ns-virtdisk-merge_virtual_disk_parameters">MERGE_VIRTUAL_DISK_PARAMETERS</a> structure that contains merge parameter data.

### -param Overlapped [in, optional]

An optional pointer to a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure if <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">asynchronous</a> operation is desired.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  All occurrences of the term <i>disk</i> in this section refer to virtual disks. The term <i>backing store</i> refers to the physical disk storage where the VHD image file or files reside.</div>
<div> </div>
The <b>MergeVirtualDisk</b> function updates all data blocks in one or more parent disks with the data blocks from the child disk referred to by the <i>VirtualDiskHandle</i> parameter. This is essentially a copy operation.

Merging a disk requires that the affected disks be detached during the operation.

The caller must have READ|WRITE access to the backing store for the affected disks.

The RWDepth of the disk must be greater than the merge depth  specified by the [OPEN_VIRTUAL_DISK_PARAMETERS](./ns-virtdisk-open_virtual_disk_parameters.md).

Merge modifies the parent disk being merged into, therefore any other differencing disks dependent on that parent will no longer be valid.

The parent disk being merged into is changed to represent the same data as was held in the child differencing disk on which the merge is performed.

Any pre-existing data in the parent disk being merged into is overwritten.

If a merge operation is interrupted, the child disk is still usable.  The <b>MergeVirtualDisk</b> function can be rerun to finish the merge.

The depth of a merge request is  the number of  parent VHD image files in the differencing chain to be merged. For example, if the <b>MergeDepth</b> member  has a value of 1, the data blocks from the specified differencing disk are moved into its parent. If the <i>MergeDepth</i> member has a value of 2 and the specified differencing disk's parent is also a differencing disk (meaning there is a third disk in the chain),  then the data blocks from both the first and second disks are moved into the third disk (with blocks from the first disk taking precedence over blocks from the second during the final operation).

Upon completion, the affected child disks are no longer considered valid, and any future operations on them will have unsupported results. In the previous example, upon successful completion of the merge, the third disk is valid and the first and second are not. The <b>MergeVirtualDisk</b> function will not delete any disks that are not valid, or perform any automatic differencing relationship reconnections. This must be explicitly done by the caller.

If a merge operation is performed on a nonleaf node of a differencing disk, it is the responsibility of the caller to fix up the parent information for the child nodes of the disk that is being merged.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>