---
UID: NI:winioctl.IOCTL_VOLUME_OFFLINE
title: IOCTL_VOLUME_OFFLINE (winioctl.h)
author: windows-sdk-content
description: Takes a volume offline.
old-location: fs\ioctl_volume_offline.htm
tech.root: FileIO
ms.assetid: 7c9b97eb-c167-41cd-b235-7a9d7830915e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_VOLUME_OFFLINE, IOCTL_VOLUME_OFFLINE control, IOCTL_VOLUME_OFFLINE control code [Files], fs.ioctl_volume_offline, winioctl/IOCTL_VOLUME_OFFLINE
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
 - IOCTL_VOLUME_OFFLINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_VOLUME_OFFLINE IOCTL


## -description


Takes a volume offline.

<b>Windows Server 2003 and Windows XP:  </b>This control code is not supported for dynamic disks.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_VOLUME_OFFLINE,         // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  NULL,                         // lpOutBuffer 
  0,                            // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped); // OVERLAPPED structure

```



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



Applications must first successfully dismount the file system - via <a href="https://msdn.microsoft.com/8828760c-9635-4c69-9867-c2f5314841e6">FSCTL_DISMOUNT_VOLUME</a> - before using <b>IOCTL_VOLUME_OFFLINE</b>.

When a volume that is online is dismounted, the next call to open the volume causes it to be mounted.  Taking the volume offline using the same volume handle as was used for the dismount prevents the dismounted volume from being mounted again.

When a volume is online, all requests sent to the volume are honored.

When a volume that is online 
    is dismounted, the next call to open the volume causes it to be mounted. Taking the volume offline prevents the 
    dismounted volume from being mounted again.

To bring a volume online, use the 
    <a href="https://msdn.microsoft.com/fa857959-c10e-4c64-8249-4bbf44e15eb9">IOCTL_VOLUME_ONLINE</a> control code.

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



<a href="https://msdn.microsoft.com/fa857959-c10e-4c64-8249-4bbf44e15eb9">IOCTL_VOLUME_ONLINE</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

