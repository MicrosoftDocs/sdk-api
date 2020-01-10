---
UID: NI:winioctl.FSCTL_GET_VOLUME_BITMAP
title: FSCTL_GET_VOLUME_BITMAP
description: Retrieves a bitmap of occupied and available clusters on a volume.
old-location: fs\fsctl_get_volume_bitmap.htm
tech.root: FileIO
ms.assetid: 80ef93ee-21a4-4766-82d2-d2ddef3ef5bb
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_VOLUME_BITMAP, FSCTL_GET_VOLUME_BITMAP control, FSCTL_GET_VOLUME_BITMAP control code [Files], _win32_fsctl_get_volume_bitmap, base.fsctl_get_volume_bitmap, fs.fsctl_get_volume_bitmap, winioctl/FSCTL_GET_VOLUME_BITMAP
f1_keywords:
- winioctl/FSCTL_GET_VOLUME_BITMAP
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_VOLUME_BITMAP IOCTL


## -description


Retrieves a bitmap of occupied and available clusters on a volume.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
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
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_move_file">FSCTL_MOVE_FILE</a> control code must be prepared for this possibility.

The handle used here must be a Volume handle and have been opened with any access. Note that only Administrators can open Volume handles.

The starting LCN in the input buffer may be rounded down before the bitmap is calculated. The rounding limit is file system dependent.

For the implications of overlapped I/O on this operation, see the Remarks section of the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

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




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/defragmenting-files">Defragmentation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_move_file">FSCTL_MOVE_FILE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-starting_lcn_input_buffer">STARTING_LCN_INPUT_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-volume_bitmap_buffer">VOLUME_BITMAP_BUFFER</a>
 

 

