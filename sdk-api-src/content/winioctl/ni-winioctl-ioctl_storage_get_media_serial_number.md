---
UID: NI:winioctl.IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
title: IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER

description: Retrieves the serial number of a USB device.
old-location: base\ioctl_storage_get_media_serial_number.htm
tech.root: devio
ms.assetid: 379c236d-c6f5-4a12-8adc-aa6377e81e6c

ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER, IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control, IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control code, _win32_ioctl_storage_get_media_serial_number, base.ioctl_storage_get_media_serial_number, winioctl/IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
ms.topic: ioctl
f1_keywords: 
 - "winioctl/IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER"
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
 - IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER IOCTL


## -description


Retrieves the serial number of a USB device.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                      // handle to device
  IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER, // dwIoControlCodeNULL,                                  // lpInBuffer0,                                     // nInBufferSize(LPVOID) lpOutBuffer,                  // output buffer
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




<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/media-serial-number-data-str">MEDIA_SERIAL_NUMBER_DATA</a>
 

 

