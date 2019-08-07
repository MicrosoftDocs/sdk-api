---
UID: NI:winioctl.FSCTL_FILESYSTEM_GET_STATISTICS_EX
title: FSCTL_FILESYSTEM_GET_STATISTICS_EX
author: windows-sdk-content
description: Retrieves the information from various file system performance counters.Support for this control code started with Windows 10.
old-location: fs\fsctl_filesystem_get_statistics_ex.htm
tech.root: FileIO
ms.assetid: 9B2C1F94-BA25-4534-BBD8-8D1EC5D05AF1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_FILESYSTEM_GET_STATISTICS_EX, FSCTL_FILESYSTEM_GET_STATISTICS_EX control, FSCTL_FILESYSTEM_GET_STATISTICS_EX control code [Files], fs.fsctl_filesystem_get_statistics_ex, winioctl/FSCTL_FILESYSTEM_GET_STATISTICS_EX
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_FILESYSTEM_GET_STATISTICS_EX
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- FSCTL_FILESYSTEM_GET_STATISTICS_EX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_FILESYSTEM_GET_STATISTICS_EX IOCTL


## -description


Retrieves the information from various file system performance counters.Support for this control code started with Windows 10.



To perform this operation, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_FILESYSTEM_GET_STATISTICS_EX,  // dwIoControlCodeNULL,                             // lpInBuffer0,                                // nInBufferSize(LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
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



In Windows 10, this code is supported by the following technologies.

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




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-filesystem_statistics_ex">FILESYSTEM_STATISTICS_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

