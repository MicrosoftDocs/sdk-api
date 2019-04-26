---
UID: NI:winioctl.FSCTL_GET_COMPRESSION
title: FSCTL_GET_COMPRESSION
author: windows-sdk-content
description: Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.
old-location: fs\fsctl_get_compression.htm
tech.root: FileIO
ms.assetid: c9932867-4b86-4119-ad13-f99aadfa559a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: COMPRESSION_FORMAT_LZNT1, COMPRESSION_FORMAT_NONE, FSCTL_GET_COMPRESSION, FSCTL_GET_COMPRESSION control, FSCTL_GET_COMPRESSION control code [Files], _win32_fsctl_get_compression, all other values, base.fsctl_get_compression, fs.fsctl_get_compression, winioctl/FSCTL_GET_COMPRESSION
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
 - FSCTL_GET_COMPRESSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_COMPRESSION IOCTL


## -description


Retrieves the current compression state of a file or directory on a volume whose file system supports 
    per-stream compression.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to file
                 FSCTL_GET_COMPRESSION,         // dwIoControlCode
                 NULL,                          // lpInBuffer 
                 0,                             // nInBufferSize
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



The LZNT1 compression algorithm is the only compression algorithm implemented.

COMPRESSION_FORMAT_DEFAULT is not a compression state so it is not included in the table under the 
    <i>lpOutBuffer</i> parameter. This value is only used with the 
    <a href="https://msdn.microsoft.com/e6fb29ed-f4f4-4507-8312-d771ffb00256">FSCTL_SET_COMPRESSION</a> control code.

If the file system of the volume containing the specified file or directory does not support per-file or 
    per-directory compression, the operation fails.

You can set the compression state of a file or directory by using the 
    <a href="https://msdn.microsoft.com/e6fb29ed-f4f4-4507-8312-d771ffb00256">FSCTL_SET_COMPRESSION</a> control code. You can also 
    compress or uncompress a file using this control code.

You can retrieve the compression attribute of a file or directory by calling the 
    <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> function. The compression attribute 
    indicates whether a file or directory is compressed. The compression state indicates whether a file or directory 
    is compressed, and, if it is, the format of the compressed data.

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
 

SMB 3.0 Transparent Failover and Scale-Out do not support NTFS compressed files. The FSCTL call is not blocked, but unsupported.





## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/e6fb29ed-f4f4-4507-8312-d771ffb00256">FSCTL_SET_COMPRESSION</a>



<a href="https://msdn.microsoft.com/35a9fb47-5a73-479c-8fe0-5a2b07705536">File Compression and Decompression</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>
 

 

