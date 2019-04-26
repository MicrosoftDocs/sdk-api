---
UID: NI:winioctl.FSCTL_GET_VOLUME_BITMAP
title: FSCTL_GET_VOLUME_BITMAP
author: windows-sdk-content
description: Retrieves a bitmap of occupied and available clusters on a volume.
old-location: fs\fsctl_get_volume_bitmap.htm
tech.root: FileIO
ms.assetid: 80ef93ee-21a4-4766-82d2-d2ddef3ef5bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_VOLUME_BITMAP, FSCTL_GET_VOLUME_BITMAP control, FSCTL_GET_VOLUME_BITMAP control code [Files], _win32_fsctl_get_volume_bitmap, base.fsctl_get_volume_bitmap, fs.fsctl_get_volume_bitmap, winioctl/FSCTL_GET_VOLUME_BITMAP
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - WinIoCtl.h
api_name:
 - FSCTL_GET_VOLUME_BITMAP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_VOLUME_BITMAP IOCTL


## -description


Retrieves a bitmap of occupied and available clusters on a volume.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to volume
  FSCTL_GET_VOLUME_BITMAP,    // dwIoControlCode(LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);</pre>
</td>
</tr>
</table></span></div>

## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



The 
<b>FSCTL_GET_VOLUME_BITMAP</b> control code retrieves a data structure that describes the allocation state of each cluster in the file system from the requested starting LCN to the last cluster on the volume. The bitmap uses one bit to represent each cluster:

<ul>
<li>The value 1 indicates that the cluster is allocated (in use).</li>
<li>The value 0 indicates that the cluster is not allocated (free).</li>
</ul>
Note that the bitmap represents a point in time, and can be incorrect as soon as it has been read if the volume has write activity. Thus, it is possible to attempt to move a cluster onto an allocated cluster in spite of a recent bitmap indicating that the cluster is unallocated. Programs using the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
<a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a> control code must be prepared for this possibility.

The handle used here must be a Volume handle and have been opened with any access. Note that only Administrators can open Volume handles.

The starting LCN in the input buffer may be rounded down before the bitmap is calculated. The rounding limit is file system dependent.

For the implications of overlapped I/O on this operation, see the Remarks section of the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> topic.

This operation aligns the bitmap it returns on a page boundary.

<b>Windows Server 2003 and Windows XP:  </b>This operation aligns the bitmap it returns on a byte boundary.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/27ccaab7-ec89-489b-80dc-df9beb7969bc">Defragmentation</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/94bdb166-fe75-4851-9dbb-a1a1f5836675">STARTING_LCN_INPUT_BUFFER</a>



<a href="https://msdn.microsoft.com/7273f469-bc5e-46b7-b908-59ddb7389c27">VOLUME_BITMAP_BUFFER</a>
 

 

