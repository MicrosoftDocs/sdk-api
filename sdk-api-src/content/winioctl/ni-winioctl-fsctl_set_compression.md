---
UID: NI:winioctl.FSCTL_SET_COMPRESSION
title: FSCTL_SET_COMPRESSION
author: windows-sdk-content
description: Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.
old-location: fs\fsctl_set_compression.htm
tech.root: FileIO
ms.assetid: e6fb29ed-f4f4-4507-8312-d771ffb00256
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: COMPRESSION_FORMAT_DEFAULT, COMPRESSION_FORMAT_LZNT1, COMPRESSION_FORMAT_NONE, FSCTL_SET_COMPRESSION, FSCTL_SET_COMPRESSION control, FSCTL_SET_COMPRESSION control code [Files], _win32_fsctl_set_compression, all other values, base.fsctl_set_compression, fs.fsctl_set_compression, winioctl/FSCTL_SET_COMPRESSION
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
 - FSCTL_SET_COMPRESSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_COMPRESSION IOCTL


## -description


Sets the compression state of a file or directory on a volume whose file system supports per-file and 
    per-directory compression. You can use 
    <b>FSCTL_SET_COMPRESSION</b> to compress or uncompress a 
    file or directory on such a volume.

To perform this operation, call the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to file or directory
                 FSCTL_SET_COMPRESSION,         // dwIoControlCode
                 (LPVOID) lpInBuffer,           // input buffer
                 (DWORD) nInBufferSize,         // size of input buffer
                 NULL,                          // lpOutBuffer
                 0,                             // nOutBufferSize
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



The LZNT1 compression algorithm is the only compression algorithm implemented. As a result, the LZNT1 
    compression algorithm is used as the DEFAULT compression method.

If the file system of the volume containing the specified file or directory does not support per-file or 
    per-directory compression, the operation fails.

The compression state change of the file or directory occurs synchronously with the call to 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>.

To retrieve the compression state of a file or directory, use the 
    <a href="https://msdn.microsoft.com/c9932867-4b86-4119-ad13-f99aadfa559a">FSCTL_GET_COMPRESSION</a> control code.

To retrieve the compression attribute of a file or directory, use the 
    <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> function. The compression attribute 
    indicates whether a file or directory is compressed. The compression state indicates whether a file or directory 
    is compressed and, if it is, the format of the compressed data.

Directories are not actually compressed by this operation. Rather, the operation sets the default state for 
    files created in the directory to be compressed.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use 
    unbuffered I/O.

File compression is supported for files of a maximum uncompressed size of 30 gigabytes.

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
See comment

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
 

CsvFs does not support making a directory compressed. CsvFs allows making file compressed only when the file is opened exclusively by a node. SMB 3.0 Transparent Failover and Scale-Out does not support NTFS compressed files. The FSCTL call is not blocked, but is unsupported."


<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
You cannot change the compression state of a file  opened with 
      <a href="https://msdn.microsoft.com/0cbc081d-8787-409b-84bc-a6a28d8f83a0">CreateFileTransacted</a>.

For more information about transactions, see 
      <a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/c9932867-4b86-4119-ad13-f99aadfa559a">FSCTL_GET_COMPRESSION</a>



<a href="https://msdn.microsoft.com/35a9fb47-5a73-479c-8fe0-5a2b07705536">File Compression and Decompression</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

