---
UID: NI:winioctl.IOCTL_STORAGE_DEVICE_POWER_CAP
title: IOCTL_STORAGE_DEVICE_POWER_CAP
description: Windows applications can use this control code to specify a maximum operational power consumption level for a storage device.helpviewer_keywords: ["IOCTL_STORAGE_DEVICE_POWER_CAP","IOCTL_STORAGE_DEVICE_POWER_CAP control","IOCTL_STORAGE_DEVICE_POWER_CAP control code [Files]","fs.ioctl_storage_device_power_cap","winioctl/IOCTL_STORAGE_DEVICE_POWER_CAP"]
old-location: fs\ioctl_storage_device_power_cap.htm
tech.root: FileIO
ms.assetid: 4BF06CA7-5219-4EE0-9A74-F43035914332
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_DEVICE_POWER_CAP, IOCTL_STORAGE_DEVICE_POWER_CAP control, IOCTL_STORAGE_DEVICE_POWER_CAP control code [Files], fs.ioctl_storage_device_power_cap, winioctl/IOCTL_STORAGE_DEVICE_POWER_CAP
f1_keywords:
- winioctl/IOCTL_STORAGE_DEVICE_POWER_CAP
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
- WinIoctl.h
api_name:
- IOCTL_STORAGE_DEVICE_POWER_CAP
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_DEVICE_POWER_CAP IOCTL


## -description


Windows applications can use this 
   control code to specify a maximum operational power  consumption level for a storage device. The OS will do it's best to transition the device to a power state that will not exceed the given maximum. However, this depends on what the device supports. The actual maximum may be less than or greater than the desired maximum.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        IOCTL_STORAGE_DEVICE_POWER_CAP, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      lpOutBuffer,     // output buffer
                    (DWORD)        nOutBufferSize,  // size of output buffer
                    (LPDWORD)      lpBytesReturned, // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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



This IOCTL is sent to the device driver with a maximum power value that the driver is expected to honor. This IOCTL then returns with a value that represents what the device driver is actually capable of achieving. This value could be equal to, less than, or greater than the desired value that was sent originally. 

For example, consider a storage device driver that implements three operational power states that have a maximum power consumption level of 10 watts, 8 watts, and 6 watts. If the caller of this IOCTL specifies that the device should not consume more than 9 watts, it must choose it's 8 watt state because that is the highest state it has that is still less than 9 watts. If the caller of this IOCTL specifies that the device should not consume more than 5 watts, the device driver will pick the 6 watt state because 6 watts is the minimum value the device can function at.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

