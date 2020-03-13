---
UID: NI:winioctl.FSCTL_QUERY_ALLOCATED_RANGES
title: FSCTL_QUERY_ALLOCATED_RANGES
description: Scans a file or alternate stream looking for ranges that may contain nonzero data.
old-location: fs\fsctl_query_allocated_ranges.htm
tech.root: FileIO
ms.assetid: 053e26ec-1529-41b3-aeb6-128b3085bafc
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_ALLOCATED_RANGES, FSCTL_QUERY_ALLOCATED_RANGES control, FSCTL_QUERY_ALLOCATED_RANGES control code [Files], _win32_fsctl_query_allocated_ranges, base.fsctl_query_allocated_ranges, fs.fsctl_query_allocated_ranges, winioctl/FSCTL_QUERY_ALLOCATED_RANGES
f1_keywords:
- winioctl/FSCTL_QUERY_ALLOCATED_RANGES
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
- FSCTL_QUERY_ALLOCATED_RANGES
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_QUERY_ALLOCATED_RANGES IOCTL


## -description


Scans a file or alternate stream looking for ranges that may contain nonzero data. Only compressed or sparse files can have zeroed ranges known to the operating system. For other files, the output buffer will contain only a single entry that contains the starting point and the length requested. 
			

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to file
  FSCTL_QUERY_ALLOCATED_RANGES,    // dwIoControlCode(LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



For the implications of overlapped I/O on this operation, see the Remarks section of 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.

The NTFS file system rounds the input file offset down to a convenient boundary and the length up to a convenient boundary and then begins to walk through the file.

The operating system does not track every piece of zero (0) or nonzero data. Because zero (0) is often a perfectly legal datum, it would be misleading. Instead, the system tracks ranges where disk space is allocated. Where no disk space is allocated, all data are assumed to be zero (0). Allocated storage can contain zero (0) or nonzero data. So all this operation does is return information about parts of the file where nonzero data may be located. It is up to the application to scan these parts of the file in accordance with the application's data conventions.

Each entry in the output array contains an offset and a length that indicates a range in the file that may contain nonzero data. The actual nonzero data, if any, is somewhere within this range, and the calling program must scan further within the range to locate it and determine if it really is valid data. Multiple instances of valid data may exist within the range.

Allocated ranges are subject to the rule that a memory mapped remote (network) file and an open handle to the file are not necessarily coherent. If you memory mapped a sparse network file and wrote nonzero data to previously unallocated regions of the file, disk space would be allocated for the new data. However, a call to 
<b>FSCTL_QUERY_ALLOCATED_RANGES</b> thereafter would not necessarily return a correct list of allocated regions. To ensure coherency between the view memory and the file handle, flush the data to the file with the 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile">FlushViewOfFile</a> function.

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




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_allocated_range_buffer">FILE_ALLOCATED_RANGE_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_zero_data">FSCTL_SET_ZERO_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/sparse-files">Sparse Files</a>
 

 

