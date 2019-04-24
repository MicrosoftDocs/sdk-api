---
UID: NI:winioctl.FSCTL_SET_ZERO_DATA
title: FSCTL_SET_ZERO_DATA
author: windows-sdk-content
description: Fills a specified range of a file with zeros (0).
old-location: fs\fsctl_set_zero_data.htm
tech.root: FileIO
ms.assetid: ee32f836-682e-4c26-b7d6-82e3b7b234f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_ZERO_DATA, FSCTL_SET_ZERO_DATA control, FSCTL_SET_ZERO_DATA control code [Files], _win32_fsctl_set_zero_data, base.fsctl_set_zero_data, fs.fsctl_set_zero_data, winioctl/FSCTL_SET_ZERO_DATA
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
 - FSCTL_SET_ZERO_DATA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_ZERO_DATA IOCTL


## -description


Fills a specified range of a file with zeros (0). If the file is sparse or compressed, the 
    NTFS file system may deallocate disk space in the file. This sets the range of bytes to zeros (0) without 
    extending the file size.

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
DeviceIoControl( (HANDLE) hDevice,              // handle to a file
                 FSCTL_SET_ZERO_DATA,           // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
                 (DWORD) nInBufferSize,         // size of input buffer
                 NULL,                          // lpOutBuffer0,                             // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
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



For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> topic.

If you use the <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function to write zeros (0) to a 
    sparse file, the file system allocates disk space for the data that you are writing. If you use the 
    <b>FSCTL_SET_ZERO_DATA</b> control code to write zeros (0) to 
    a sparse file and the zero (0)  region is large enough, the file system may not allocate disk space.

If you use the <b>FSCTL_SET_ZERO_DATA</b> control code to 
    write zeros (0) to a non-sparse file, zeros (0) are written to the file. The system allocates disk storage for all 
    of the zero (0) range, which is equivalent to using the 
    <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function to write zeros (0) to a file.

The time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered 
    I/O.

IIn Windows 8 and Windows Server 2012, this code is supported by the following technologies.

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
Yes

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/ad2c4e2d-7f41-45e8-beff-2f6d735f152e">FILE_ZERO_DATA_INFORMATION</a>



<a href="https://msdn.microsoft.com/053e26ec-1529-41b3-aeb6-128b3085bafc">FSCTL_QUERY_ALLOCATED_RANGES</a>



<a href="https://msdn.microsoft.com/aa8f5880-f831-49b6-8359-fe07c78c032f">FSCTL_SET_SPARSE</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>



<a href="https://msdn.microsoft.com/7326041d-f11e-4b80-ac4e-07173e418ce7">Sparse Files</a>
 

 

