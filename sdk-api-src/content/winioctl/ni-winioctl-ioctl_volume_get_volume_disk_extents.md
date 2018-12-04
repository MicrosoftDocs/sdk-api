---
UID: NI:winioctl.IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
title: IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
author: windows-sdk-content
description: Retrieves the physical location of a specified volume on one or more disks.
old-location: fs\ioctl_volume_get_volume_disk_extents.htm
tech.root: fileio
ms.assetid: 8faff037-d815-48f8-8b59-d63f4ff4a746
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS control, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS control code [Files], _win32_ioctl_volume_get_volume_disk_extents, base.ioctl_volume_get_volume_disk_extents, fs.ioctl_volume_get_volume_disk_extents, winioctl/IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS IOCTL


## -description


Retrieves the physical location of a specified volume on one or more disks.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,                     // handle to device
                 IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, // dwIoControlCodeNULL,                                 // lpInBuffer0,                                    // nInBufferSize(LPVOID) lpOutBuffer,                 // output buffer
                 (DWORD) nOutBufferSize,               // size of output buffer
                 (LPDWORD) lpBytesReturned,            // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped           // OVERLAPPED structure
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/3f38f03c-1b99-4072-904c-dca1b98a245c">VOLUME_DISK_EXTENTS</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

