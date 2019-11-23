---
UID: NI:winioctl.FSCTL_FILE_LEVEL_TRIM
title: FSCTL_FILE_LEVEL_TRIM

description: Indicates to the storage system which ranges in the file are not needed to be stored.
old-location: fs\fsctl_file_level_trim.htm
tech.root: FileIO
ms.assetid: 2d466a98-f7b2-4638-942c-1cf9016d0bf9

ms.date: 12/05/2018
ms.keywords: FSCTL_FILE_LEVEL_TRIM, FSCTL_FILE_LEVEL_TRIM control, FSCTL_FILE_LEVEL_TRIM control code [Files], fs.fsctl_file_level_trim, winioctl/FSCTL_FILE_LEVEL_TRIM
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_FILE_LEVEL_TRIM
dev_langs:
 - c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- FSCTL_FILE_LEVEL_TRIM
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_FILE_LEVEL_TRIM IOCTL


## -description


Indicates to the storage system which ranges in the file are not needed to be stored.

To perform this operation, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 (DWORD) FSCTL_FILE_LEVEL_TRIM, // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



The <b>FSCTL_FILE_LEVEL_TRIM</b> control code is a hint 
    to the underlying storage system. When a range of bytes has been trimmed, if that range is later read again the 
    data returned may be the original data before the trim operation, all zeros (0x00 bytes), all ones (0xff bytes), 
    or some combination of these. Before the trim operation is passed to the underlying storage system the input 
    ranges are reduced to be aligned to page boundaries (4,096 bytes on 32-bit and x64-based editions of Windows, 
    8,192 bytes on Itanium-Based  editions of Windows).

If an error occurs while processing the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_range">FILE_LEVEL_TRIM_RANGE</a> entries that follow the 
    <b>FILE_LEVEL_TRIM</b> structure in the input buffer pointed 
    to by the <i>lpInBuffer</i> parameter, processing stops and the 
    <b>NumRangesProcessed</b> member of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_output">FILE_LEVEL_TRIM_OUTPUT</a> structure pointed to by the 
    <i>lpOutBuffer</i> parameter will be indicate which ranges were successfully processed. Any 
    ranges between <b>NumRangesProcessed</b> and the <b>NumRanges</b> member 
    of the <b>FILE_LEVEL_TRIM</b> structure were not 
    processed.

The <b>FSCTL_FILE_LEVEL_TRIM</b> control code is not 
    compatible with encrypted or compressed files 
    (<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a> returns 
    <b>FILE_ATTRIBUTE_ENCRYPTED</b> or <b>FILE_ATTRIBUTE_COMPRESSED</b>) and 
    will fail with <b>ERROR_INVALID_PARAMETER</b>. Sparse files (indicated by 
    <b>FILE_ATTRIBUTE_SPARSE_FILE</b>) are supported, but only ranges that have been allocated can 
    be trimmed. While individually encrypted files are not supported, files on volumes encrypted by BitLocker 
    technology are supported.

The <b>FSCTL_FILE_LEVEL_TRIM</b> control code does not 
    participate in transactions. If a 
    <b>FSCTL_FILE_LEVEL_TRIM</b> control code is processed 
    during a transaction, and the transaction is aborted, the trim will not be rolled back with the transaction.

Ranges that are successfully trimmed will be removed from the filesystem cache.

Ranges that are trimmed can be beyond the valid data length (VDL) up to the end-of-file (EOF).

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
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

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
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_file_level_trim">FILE_LEVEL_TRIM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_output">FILE_LEVEL_TRIM_OUTPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

