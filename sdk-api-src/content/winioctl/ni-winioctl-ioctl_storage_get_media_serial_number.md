---
UID: NI:winioctl.IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
title: IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
author: windows-sdk-content
description: Retrieves the serial number of a USB device.
old-location: base\ioctl_storage_get_media_serial_number.htm
old-project: devio
ms.assetid: 379c236d-c6f5-4a12-8adc-aa6377e81e6c
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER, IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control, IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control code, _win32_ioctl_storage_get_media_serial_number, base.ioctl_storage_get_media_serial_number, winioctl/IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
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
tech.root: 
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER IOCTL


## -description


Retrieves the serial number of a USB device.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL DeviceIoControl(
  (HANDLE) hDevice,                      // handle to device
  IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER, // dwIoControlCode
  NULL,                                  // lpInBuffer
  0,                                     // nInBufferSize
  (LPVOID) lpOutBuffer,                  // output buffer
  (DWORD) nOutBufferSize,                // size of output buffer
  (LPDWORD) lpBytesReturned,             // number of bytes returned
  (LPOVERLAPPED) lpOverlapped            // OVERLAPPED structure
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




## -see-also




<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562213">MEDIA_SERIAL_NUMBER_DATA</a>
 

 

