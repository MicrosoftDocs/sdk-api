---
UID: NI:winioctl.IOCTL_STORAGE_GET_DEVICE_NUMBER
title: IOCTL_STORAGE_GET_DEVICE_NUMBER
description: Retrieves the device type, device number, and, for a partitionable device, the partition number of a device.
old-location: base\ioctl_storage_get_device_number.htm
tech.root: devio
ms.assetid: 2cd9610b-aa83-4d0a-a7a9-1d4dab8be331
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_DEVICE_NUMBER, IOCTL_STORAGE_GET_DEVICE_NUMBER control, IOCTL_STORAGE_GET_DEVICE_NUMBER control code, base.ioctl_storage_get_device_number, winioctl/IOCTL_STORAGE_GET_DEVICE_NUMBER
f1_keywords:
- winioctl/IOCTL_STORAGE_GET_DEVICE_NUMBER
dev_langs:
- c++
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
- IOCTL_STORAGE_GET_DEVICE_NUMBER
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_GET_DEVICE_NUMBER IOCTL


## -description


Retrieves the device type, device number, and, for a partitionable device, the partition number of a device. 

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
  (HANDLE) hDevice,                // handle to device
  IOCTL_STORAGE_GET_DEVICE_NUMBER, // dwIoControlCodeNULL,                            // lpInBuffer0,                               // nInBufferSize(LPVOID), lpOutBuffer,           // output buffer
  (DWORD), nOutBufferSize,         // size of output buffer
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



The values in the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_device_number">STORAGE_DEVICE_NUMBER</a> structure are guaranteed to remain unchanged until the device is removed or the system is restarted. It is not guaranteed to be persistent across device restarts or system restarts. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_device_number">STORAGE_DEVICE_NUMBER</a>
 

 

