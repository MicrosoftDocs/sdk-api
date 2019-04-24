---
UID: NI:winioctl.FSCTL_SET_REPARSE_POINT
title: FSCTL_SET_REPARSE_POINT
author: windows-sdk-content
description: Sets a reparse point on a file or directory.
old-location: fs\fsctl_set_reparse_point.htm
tech.root: FileIO
ms.assetid: 0bed6d69-269b-4921-8984-69c7829fb9ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_REPARSE_POINT, FSCTL_SET_REPARSE_POINT control, FSCTL_SET_REPARSE_POINT control code [Files], _win32_fsctl_set_reparse_point, base.fsctl_set_reparse_point, fs.fsctl_set_reparse_point, winioctl/FSCTL_SET_REPARSE_POINT
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
 - FSCTL_SET_REPARSE_POINT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_REPARSE_POINT IOCTL


## -description


Sets a reparse point on a file or directory.

To perform this operation, call the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,              // handle to file or directory
                      FSCTL_SET_REPARSE_POINT,       // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer 
                      (DWORD) nInBufferSize,         // size of input buffer
                      NULL,                          // lpOutBuffer0,                             // nOutBufferSizeNULL,                          // lpBytesReturned(LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure</pre>
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
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use 
    unbuffered I/O.

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




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/f582f3e3-56bd-4a21-817e-233ff0fece6e">FSCTL_DELETE_REPARSE_POINT</a>



<a href="https://msdn.microsoft.com/6f1b7ea2-aed6-4ab4-8e92-1b77ab5cfefb">FSCTL_GET_REPARSE_POINT</a>



<a href="https://msdn.microsoft.com/e906a874-51f1-4623-8f0b-afdfd8169ab2">REPARSE_DATA_BUFFER</a>



<a href="https://msdn.microsoft.com/2d49c1bc-0b1d-40b1-a3a2-6b30f0b3cca0">REPARSE_GUID_DATA_BUFFER</a>



<a href="https://msdn.microsoft.com/3abb3a08-9a00-43eb-9792-82eab1a25f06">Reparse Points</a>
 

 

