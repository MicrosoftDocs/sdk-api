---
UID: NI:winioctl.FSCTL_GET_REPARSE_POINT
title: FSCTL_GET_REPARSE_POINT
author: windows-sdk-content
description: Retrieves the reparse point data associated with the file or directory identified by the specified handle.
old-location: fs\fsctl_get_reparse_point.htm
tech.root: FileIO
ms.assetid: 6f1b7ea2-aed6-4ab4-8e92-1b77ab5cfefb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_REPARSE_POINT, FSCTL_GET_REPARSE_POINT control, FSCTL_GET_REPARSE_POINT control code [Files], _win32_fsctl_get_reparse_point, base.fsctl_get_reparse_point, fs.fsctl_get_reparse_point, winioctl/FSCTL_GET_REPARSE_POINT
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
 - FSCTL_GET_REPARSE_POINT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_REPARSE_POINT IOCTL


## -description


Retrieves the reparse point data associated with the file or directory identified by the specified handle.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to file or directory
  FSCTL_GET_REPARSE_POINT,     // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSize(LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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



For the implications of overlapped I/O on this operation, see the Remarks section of 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.

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
No

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
 

CsvFs does not support reparse points.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_delete_reparse_point">FSCTL_DELETE_REPARSE_POINT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_reparse_point">FSCTL_SET_REPARSE_POINT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_reparse_guid_data_buffer">REPARSE_GUID_DATA_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/reparse-points">Reparse Points</a>
 

 

