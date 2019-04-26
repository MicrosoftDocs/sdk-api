---
UID: NI:winioctl.FSCTL_INITIATE_REPAIR
title: FSCTL_INITIATE_REPAIR
author: windows-sdk-content
description: Triggers the NTFS file system to start a self-healing cycle on a single file.
old-location: fs\fsctl_initiate_repair.htm
tech.root: FileIO
ms.assetid: 948f6c3e-34ac-4270-bb2f-dc2ffd111005
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_INITIATE_REPAIR, FSCTL_INITIATE_REPAIR control, FSCTL_INITIATE_REPAIR control code [Files], fs.fsctl_initiate_repair, winioctl/FSCTL_INITIATE_REPAIR
ms.topic: ioctl
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
 - FSCTL_INITIATE_REPAIR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_INITIATE_REPAIR IOCTL


## -description


Triggers the NTFS file system to start a self-healing cycle on a single file.

To perform this operation, call the 
   <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_INITIATE_REPAIR, // dwIoControlCode(PLONGLONG) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  NULL,                         // output buffer
  0,                            // size of output buffer
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
No

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
 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/25c9ffdf-2839-46aa-b1fe-ce1383a3a813">FSCTL_GET_REPAIR</a>



<a href="https://msdn.microsoft.com/3df03a87-7117-4f85-a04e-54bcd800e8ff">FSCTL_SET_REPAIR</a>



<a href="https://msdn.microsoft.com/593ca2f0-1455-4b46-925a-61ad07f8fb5c">FSCTL_WAIT_FOR_REPAIR</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>
 

 

