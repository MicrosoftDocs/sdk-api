---
UID: NI:winioctl.FSCTL_QUERY_ON_DISK_VOLUME_INFO
title: FSCTL_QUERY_ON_DISK_VOLUME_INFO
author: windows-sdk-content
description: Requests UDF-specific volume information.
old-location: fs\fsctl_query_on_disk_volume_info.htm
tech.root: FileIO
ms.assetid: 6d34007e-4e6f-433e-9d85-9b2743e1c1d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_ON_DISK_VOLUME_INFO, FSCTL_QUERY_ON_DISK_VOLUME_INFO control, FSCTL_QUERY_ON_DISK_VOLUME_INFO control code [Files], fs.fsctl_query_on_disk_volume_info, winioctl/FSCTL_QUERY_ON_DISK_VOLUME_INFO
ms.topic: ioctl
f1_keywords: 
 - "winioctl/FSCTL_QUERY_ON_DISK_VOLUME_INFO"
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FSCTL_QUERY_ON_DISK_VOLUME_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_QUERY_ON_DISK_VOLUME_INFO IOCTL


## -description


Requests UDF-specific volume information.

To perform this operation, call the 
   <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_QUERY_ON_DISK_VOLUME_INFO, // dwIoControlCodeNULL,                       // input buffer
  0,                          // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
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
No

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_file_query_on_disk_vol_info_buffer">FILE_QUERY_ON_DISK_VOL_INFO_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

