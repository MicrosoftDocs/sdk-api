---
UID: NI:winioctl.IOCTL_VOLUME_ONLINE
title: IOCTL_VOLUME_ONLINE
description: Brings a volume online.helpviewer_keywords: ["IOCTL_VOLUME_ONLINE","IOCTL_VOLUME_ONLINE control","IOCTL_VOLUME_ONLINE control code [Files]","fs.ioctl_volume_online","winioctl/IOCTL_VOLUME_ONLINE"]
old-location: fs\ioctl_volume_online.htm
tech.root: FileIO
ms.assetid: fa857959-c10e-4c64-8249-4bbf44e15eb9
ms.date: 12/05/2018
ms.keywords: IOCTL_VOLUME_ONLINE, IOCTL_VOLUME_ONLINE control, IOCTL_VOLUME_ONLINE control code [Files], fs.ioctl_volume_online, winioctl/IOCTL_VOLUME_ONLINE
f1_keywords:
- winioctl/IOCTL_VOLUME_ONLINE
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
- IOCTL_VOLUME_ONLINE
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_VOLUME_ONLINE IOCTL


## -description


Brings a volume online.

<b>Windows Server 2003 and Windows XP:  </b>This control code is not supported for dynamic disks.

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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



When a volume is offline, all read, write, and IOCTL requests fail with <b>ERROR_NOT_READY</b>. You cannot take the system or boot volume offline.

When a volume is online, all requests sent to the volume are honored.

When a volume that is online is dismounted, the next call to open the volume causes it to be mounted. Taking the volume offline prevents the dismounted volume from being mounted again.

To take a volume offline, use the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_offline">IOCTL_VOLUME_OFFLINE</a> control code.

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




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_offline">IOCTL_VOLUME_OFFLINE</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
 

 

