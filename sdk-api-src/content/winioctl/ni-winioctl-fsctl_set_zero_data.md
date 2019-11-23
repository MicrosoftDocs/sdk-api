---
UID: NI:winioctl.FSCTL_SET_ZERO_DATA
title: FSCTL_SET_ZERO_DATA

description: Fills a specified range of a file with zeros (0).
old-location: fs\fsctl_set_zero_data.htm
tech.root: FileIO
ms.assetid: ee32f836-682e-4c26-b7d6-82e3b7b234f9

ms.date: 12/05/2018
ms.keywords: FSCTL_SET_ZERO_DATA, FSCTL_SET_ZERO_DATA control, FSCTL_SET_ZERO_DATA control code [Files], _win32_fsctl_set_zero_data, base.fsctl_set_zero_data, fs.fsctl_set_zero_data, winioctl/FSCTL_SET_ZERO_DATA
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_SET_ZERO_DATA
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
- FSCTL_SET_ZERO_DATA
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_ZERO_DATA IOCTL


## -description


Fills a specified range of a file with zeros (0). If the file is sparse or compressed, the 
    NTFS file system may deallocate disk space in the file. This sets the range of bytes to zeros (0) without 
    extending the file size.

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
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

If you use the <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> function to write zeros (0) to a 
    sparse file, the file system allocates disk space for the data that you are writing. If you use the 
    <b>FSCTL_SET_ZERO_DATA</b> control code to write zeros (0) to 
    a sparse file and the zero (0)  region is large enough, the file system may not allocate disk space.

If you use the <b>FSCTL_SET_ZERO_DATA</b> control code to 
    write zeros (0) to a non-sparse file, zeros (0) are written to the file. The system allocates disk storage for all 
    of the zero (0) range, which is equivalent to using the 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> function to write zeros (0) to a file.

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




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_zero_data_information">FILE_ZERO_DATA_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges">FSCTL_QUERY_ALLOCATED_RANGES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/sparse-files">Sparse Files</a>
 

 

