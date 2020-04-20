---
UID: NI:winioctl.FSCTL_GET_RETRIEVAL_POINTERS
title: FSCTL_GET_RETRIEVAL_POINTERS
description: Given a file handle, retrieves a data structure that describes the allocation and location on disk of a specific file, or, given a volume handle, the locations of bad clusters on a volume.helpviewer_keywords: ["FSCTL_GET_RETRIEVAL_POINTERS","FSCTL_GET_RETRIEVAL_POINTERS control","FSCTL_GET_RETRIEVAL_POINTERS control code [Files]","_win32_fsctl_get_retrieval_pointers","base.fsctl_get_retrieval_pointers","fs.fsctl_get_retrieval_pointers","winioctl/FSCTL_GET_RETRIEVAL_POINTERS"]
old-location: fs\fsctl_get_retrieval_pointers.htm
tech.root: FileIO
ms.assetid: 002f6703-8db3-4034-a79f-3fa9c4159115
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_RETRIEVAL_POINTERS, FSCTL_GET_RETRIEVAL_POINTERS control, FSCTL_GET_RETRIEVAL_POINTERS control code [Files], _win32_fsctl_get_retrieval_pointers, base.fsctl_get_retrieval_pointers, fs.fsctl_get_retrieval_pointers, winioctl/FSCTL_GET_RETRIEVAL_POINTERS
f1_keywords:
- winioctl/FSCTL_GET_RETRIEVAL_POINTERS
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
- FSCTL_GET_RETRIEVAL_POINTERS
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_RETRIEVAL_POINTERS IOCTL


## -description


Given a file handle, retrieves a data structure that describes the allocation and location on disk of a specific 
    file, or, given a volume handle, the locations of bad clusters on a volume.

To perform this operation, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DeviceIoControl(
  (HANDLE) hDevice,              // handle to file, directory, or volume
  FSCTL_GET_RETRIEVAL_POINTERS,  // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  (LPVOID) lpOutBuffer,          // output buffer
  (DWORD) nOutBufferSize,        // size of output buffer
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure</pre>
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



The 
<b>FSCTL_GET_RETRIEVAL_POINTERS</b> operation retrieves a variably sized data structure that describes the allocation and location on disk of a specific file. The structure describes the mapping between virtual cluster numbers (VCN offsets within the file or stream space) and logical cluster numbers (LCN offsets within the volume space).

The <b>FSCTL_GET_RETRIEVAL_POINTERS</b> control code is supported for file or directory operations on NTFS, FAT, exFAT, and UDF file systems.

On supported file systems, the <b>FSCTL_GET_RETRIEVAL_POINTERS</b> operation returns the extent locations of nonresident data.  Resident data never has extent locations.

The <b>FSCTL_GET_RETRIEVAL_POINTERS</b> control code also supports the alternate functionality of locating bad clusters. To query for the locations of bad clusters on a volume formatted with NTFS, FAT, or exFAT, use a volume handle as the <i>hDevice</i> parameter. This functionality is supported only on NTFS, FAT, and exFAT, and the caller must have <b>MANAGE_VOLUME_ACCESS</b> permission to the volume.

For the implications of overlapped I/O on this operation, see the Remarks section of the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

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



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointer_base">FSCTL_GET_RETRIEVAL_POINTER_BASE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-retrieval_pointers_buffer">RETRIEVAL_POINTERS_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-starting_vcn_input_buffer">STARTING_VCN_INPUT_BUFFER</a>
 

 

