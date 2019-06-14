---
UID: NI:winioctl.IOCTL_STORAGE_FIRMWARE_ACTIVATE
title: IOCTL_STORAGE_FIRMWARE_ACTIVATE
author: windows-sdk-content
description: Windows applications can use this control code to activate a firmware image on a specified device.
old-location: fs\ioctl_storage_firmware_activate.htm
tech.root: FileIO
ms.assetid: 000BEB58-D91E-4859-AC31-A4C72B84A982
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_FIRMWARE_ACTIVATE, IOCTL_STORAGE_FIRMWARE_ACTIVATE control, IOCTL_STORAGE_FIRMWARE_ACTIVATE control code [Files], fs.ioctl_storage_firmware_activate, winioctl/IOCTL_STORAGE_FIRMWARE_ACTIVATE
ms.topic: ioctl
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
 - IOCTL_STORAGE_FIRMWARE_ACTIVATE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_FIRMWARE_ACTIVATE IOCTL


## -description


Windows applications can use this control code to activate a firmware image on a specified device.

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
                    (DWORD)        IOCTL_STORAGE_FIRMWARE_ACTIVATE, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_download">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_get_info">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_hw_firmware_activate">STORAGE_HW_FIRMWARE_ACTIVATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_hw_firmware_download">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/storage-hw-firmware-info">STORAGE_HW_FIRMWARE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/storage-hw-firmware-info-query">STORAGE_HW_FIRMWARE_INFO_QUERY</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/storage-hw-firmware-slot-info">STORAGE_HW_FIRMWARE_SLOT_INFO</a>
 

 

