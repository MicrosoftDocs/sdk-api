---
UID: NF:vdssys.CompactVirtualDisk
title: CompactVirtualDisk function
author: windows-sdk-content
description: Reduces the size of a virtual hard disk (VHD) backing store file.
old-location: vhd\compactvirtualdisk.htm
old-project: VStor
ms.assetid: 8f887ef9-6be5-455a-8904-2047f2efe13c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CompactVirtualDisk, CompactVirtualDisk function [VHD], vdssys/CompactVirtualDisk, vhd.compactvirtualdisk, virtdisk/CompactVirtualDisk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vdssys.h
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
tech.root: 
req.typenames: VIRTUAL_DISK_ACCESS_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	VirtDisk.dll
api_name:
-	CompactVirtualDisk
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# CompactVirtualDisk function


## -description


Reduces the size of a virtual hard disk (VHD) backing store file.


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the 
      <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag in the 
      <i>VirtualDiskAccessMask</i> parameter passed to 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a>. For information on how to open a 
      virtual disk, see the <b>OpenVirtualDisk</b> function.


### -param Flags [in]

Must be the <b>COMPACT_VIRTUAL_DISK_FLAG_NONE</b> value (0) of the 
      <a href="https://msdn.microsoft.com/e0efa6e3-e691-4854-a09e-9504a37621a2">COMPACT_VIRTUAL_DISK_FLAG</a> enumeration.


### -param Parameters [in, optional]

A optional pointer to a valid 
      <a href="https://msdn.microsoft.com/3e58101c-c8a9-432e-99c4-9e418a887b9e">COMPACT_VIRTUAL_DISK_PARAMETERS</a> 
      structure that contains compaction parameter data.


### -param Overlapped [in, optional]

An optional pointer to a valid <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> 
      structure if <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">asynchronous</a> 
      operation is desired.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Compaction can be run only on a virtual disk that is dynamically expandable or differencing.

There are two different types of compaction.

<ul>
<li>The first type, file-system-aware compaction, uses the NTFS file system to determine free space. This is 
      done by attaching the VHD as a read-only device by including the 
      <b>VIRTUAL_DISK_ACCESS_METAOPS</b> and 
      <b>VIRTUAL_DISK_ACCESS_ATTACH_RO</b> flags in the 
      <i>VirtualDiskAccessMask</i> parameter passed to 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a>, attaching the VHD by calling 
      <a href="https://msdn.microsoft.com/528370bc-77d4-4983-8910-d941165a037c">AttachVirtualDisk</a>, and while the VHD is attached 
      calling <b>CompactVirtualDisk</b>. Detaching the VHD 
      before compaction is done can cause compaction to return failure before it is done (similar to cancellation of 
      compaction).</li>
<li>The second type, file-system-agnostic compaction, does not involve the file system but only looks for VHD 
      blocks filled entirely with zeros (0). This is done by including the 
      <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag in the 
      <i>VirtualDiskAccessMask</i> parameter passed to 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a>, and calling 
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




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

