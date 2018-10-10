---
UID: NI:winioctl.IOCTL_VOLUME_ONLINE
title: IOCTL_VOLUME_ONLINE
author: windows-sdk-content
description: Brings a volume online.
old-location: fs\ioctl_volume_online.htm
tech.root: fileio
ms.assetid: fa857959-c10e-4c64-8249-4bbf44e15eb9
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IOCTL_VOLUME_ONLINE, IOCTL_VOLUME_ONLINE control, IOCTL_VOLUME_ONLINE control code [Files], fs.ioctl_volume_online, winioctl/IOCTL_VOLUME_ONLINE
ms.prod: windows
ms.technology: windows-sdk
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
 - IOCTL_VOLUME_ONLINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_VOLUME_ONLINE IOCTL


## -description


Brings a volume online.

<b>Windows Server 2003 and Windows XP:  </b>This control code is not supported for dynamic disks.

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
  IOCTL_VOLUME_ONLINE,          // dwIoControlCodeNULL,                         // lpInBuffer0,                            // nInBufferSizeNULL,                         // lpOutBuffer0,                            // nOutBufferSize(LPDWORD) lpBytesReturned,    // number of bytes returned
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



When a volume is offline, all read, write, and IOCTL requests fail with <b>ERROR_NOT_READY</b>. You cannot take the system or boot volume offline.

When a volume is online, all requests sent to the volume are honored.

When a volume that is online is dismounted, the next call to open the volume causes it to be mounted. Taking the volume offline prevents the dismounted volume from being mounted again.

To take a volume offline, use the <a href="https://msdn.microsoft.com/7c9b97eb-c167-41cd-b235-7a9d7830915e">IOCTL_VOLUME_OFFLINE</a> control code.

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
No

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/7c9b97eb-c167-41cd-b235-7a9d7830915e">IOCTL_VOLUME_OFFLINE</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

