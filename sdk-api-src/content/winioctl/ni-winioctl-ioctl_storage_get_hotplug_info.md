---
UID: NI:winioctl.IOCTL_STORAGE_GET_HOTPLUG_INFO
title: IOCTL_STORAGE_GET_HOTPLUG_INFO
author: windows-sdk-content
description: Retrieves the hotplug configuration of the specified device.
old-location: base\ioctl_storage_get_hotplug_info.htm
tech.root: devio
ms.assetid: 4ecf6f84-17fc-4c48-a859-c043e8f9cd14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_HOTPLUG_INFO, IOCTL_STORAGE_GET_HOTPLUG_INFO control, IOCTL_STORAGE_GET_HOTPLUG_INFO control code, _win32_ioctl_storage_get_hotplug_info, base.ioctl_storage_get_hotplug_info, winioctl/IOCTL_STORAGE_GET_HOTPLUG_INFO
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_STORAGE_GET_HOTPLUG_INFO
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
- IOCTL_STORAGE_GET_HOTPLUG_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_GET_HOTPLUG_INFO IOCTL


## -description


Retrieves the hotplug configuration of the specified device.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_STORAGE_GET_HOTPLUG_INFO,  // dwIoControlCodeNULL,                            // lpInBuffer0,                               // nInBufferSize(LPVOID) lpOutBuffer,            // output buffer
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



Refer to the Remarks section in the reference page for 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_hotplug_info">STORAGE_HOTPLUG_INFO</a> for more information about hotplug devices.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_hotplug_info">IOCTL_STORAGE_SET_HOTPLUG_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_hotplug_info">STORAGE_HOTPLUG_INFO</a>
 

 

