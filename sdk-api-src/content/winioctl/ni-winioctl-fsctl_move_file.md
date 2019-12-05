---
UID: NI:winioctl.FSCTL_MOVE_FILE
title: FSCTL_MOVE_FILE
description: Relocates one or more virtual clusters of a file from one logical cluster to another within the same volume. This operation is used during defragmentation.
old-location: fs\fsctl_move_file.htm
tech.root: FileIO
ms.assetid: ab7f81ac-a962-4e86-b426-b0082d251645
ms.date: 12/05/2018
ms.keywords: FSCTL_MOVE_FILE, FSCTL_MOVE_FILE control, FSCTL_MOVE_FILE control code [Files], _win32_fsctl_move_file, base.fsctl_move_file, fs.fsctl_move_file, winioctl/FSCTL_MOVE_FILE
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_MOVE_FILE
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
- FSCTL_MOVE_FILE
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_MOVE_FILE IOCTL


## -description


Relocates one or more virtual clusters of a file from one logical cluster to another within the same 
    volume. This operation is used during 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/defragmenting-files">defragmentation</a>.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to volume
                 (DWORD)        FSCTL_MOVE_FILE, // dwIoControlCode
                 (LPVOID)       lpInBuffer,      // MOVE_FILE_DATA structure
                 (DWORD)        nInBufferSize,   // size of input buffer
                 (LPVOID)       NULL,            // lpOutBuffer
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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



The <b>FSCTL_MOVE_FILE</b> control code relocates one or more 
    virtual clusters of a file from one logical cluster to another within the same volume. If the file to be moved is 
    a sparse or compressed file, the granularity of the move is 16 clusters; otherwise, the granularity is one 
    cluster.

To mark an open  file so that it is not defragmented, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_mark_handle">FSCTL_MARK_HANDLE</a> control code with 
    <b>MARK_HANDLE_PROTECT_CLUSTERS</b> in the <b>HandleInfo</b> member of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-mark_handle_info">MARK_HANDLE_INFO</a> structure passed in the 
    <i>lpInBuffer</i> parameter.

Note that the bitmap returned by the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap">FSCTL_GET_VOLUME_BITMAP</a> control code represents a 
    point in time, and can be incorrect as soon as it has been read if the volume has write activity. Thus, it is 
    possible to attempt to move a cluster onto an allocated cluster in spite of a recent bitmap indicating that the 
    cluster is unallocated. Programs using <b>FSCTL_MOVE_FILE</b> must 
    be prepared for this possibility.

For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

For a list of files, streams, and stream types supported by the 
    <b>FSCTL_MOVE_FILE</b> control code, see the 
    <a href="/windows/win32/fileio/defragmenting-files#files-streams-and-stream-types-supported-for-defragmentation">Files, streams, and stream types supported for defragmentation</a> 
    section of the <a href="https://docs.microsoft.com/windows/desktop/FileIO/defragmenting-files">Defragmenting Files</a> 
    topic.

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



<a href="https://docs.microsoft.com/windows/desktop/FileIO/defragmenting-files">Defragmenting Files</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap">FSCTL_GET_VOLUME_BITMAP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-move_file_data">MOVE_FILE_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>
 

 

