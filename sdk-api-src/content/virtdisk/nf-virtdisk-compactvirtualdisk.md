---
UID: NF:virtdisk.CompactVirtualDisk
title: CompactVirtualDisk function (virtdisk.h)
description: Reduces the size of a virtual hard disk (VHD) backing store file.
helpviewer_keywords: ["CompactVirtualDisk","CompactVirtualDisk function [VHD]","vdssys/CompactVirtualDisk","vhd.compactvirtualdisk","virtdisk/CompactVirtualDisk"]
old-location: vhd\compactvirtualdisk.htm
tech.root: VStor
ms.assetid: 8f887ef9-6be5-455a-8904-2047f2efe13c
ms.date: 12/05/2018
ms.keywords: CompactVirtualDisk, CompactVirtualDisk function [VHD], vdssys/CompactVirtualDisk, vhd.compactvirtualdisk, virtdisk/CompactVirtualDisk
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
 - CompactVirtualDisk
 - virtdisk/CompactVirtualDisk
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
 - CompactVirtualDisk
---

# CompactVirtualDisk function


## -description

Reduces the size of a virtual hard disk (VHD) backing store file.

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the 
      <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag in the 
      <i>VirtualDiskAccessMask</i> parameter passed to 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a>. For information on how to open a 
      virtual disk, see the <b>OpenVirtualDisk</b> function.

### -param Flags [in]

Must be the <b>COMPACT_VIRTUAL_DISK_FLAG_NONE</b> value (0) of the 
      <a href="/windows/win32/api/virtdisk/ne-virtdisk-compact_virtual_disk_flag">COMPACT_VIRTUAL_DISK_FLAG</a> enumeration.

### -param Parameters [in, optional]

A optional pointer to a valid 
      <a href="/windows/win32/api/virtdisk/ns-virtdisk-compact_virtual_disk_parameters">COMPACT_VIRTUAL_DISK_PARAMETERS</a> 
      structure that contains compaction parameter data.

### -param Overlapped [in, optional]

An optional pointer to a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> 
      structure if <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">asynchronous</a> 
      operation is desired.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

Compaction can be run only on a virtual disk that is dynamically expandable or differencing.

There are two different types of compaction.

<ul>
<li>The first type, file-system-aware compaction, uses the NTFS file system to determine free space. This is 
      done by attaching the VHD as a read-only device by including the 
      <b>VIRTUAL_DISK_ACCESS_METAOPS</b> and 
      <b>VIRTUAL_DISK_ACCESS_ATTACH_RO</b> flags in the 
      <i>VirtualDiskAccessMask</i> parameter passed to 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a>, attaching the VHD by calling 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk">AttachVirtualDisk</a>, and while the VHD is attached 
      calling <b>CompactVirtualDisk</b>. Detaching the VHD 
      before compaction is done can cause compaction to return failure before it is done (similar to cancellation of 
      compaction).</li>
<li>The second type, file-system-agnostic compaction, does not involve the file system but only looks for VHD 
      blocks filled entirely with zeros (0). This is done by including the 
      <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag in the 
      <i>VirtualDiskAccessMask</i> parameter passed to 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a>, and calling 
      <b>CompactVirtualDisk</b>.</li>
</ul>
File-system-aware compaction is the most efficient compaction type but using first the file-system-aware 
    compaction followed by the file-system-agnostic compaction will produce the smallest VHD.

A compaction operation on a virtual disk can be safely interrupted and re-run later. Re-opening a virtual disk 
    file that has been interrupted may result in the reduction of a virtual disk file's size at the time of 
    opening.

Compaction can be CPU-intensive and/or I/O-intensive, depending on how large the virtual disk is and how many 
    blocks require movement.

The <b>CompactVirtualDisk</b> function runs on the 
    virtual disk in the same security context as the caller.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>