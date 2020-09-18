---
UID: NI:winioctl.IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
title: IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
description: Retrieves the serial number of a USB device.
helpviewer_keywords: ["IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER","IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control","IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control code","_win32_ioctl_storage_get_media_serial_number","base.ioctl_storage_get_media_serial_number","winioctl/IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER"]
old-location: base\ioctl_storage_get_media_serial_number.htm
tech.root: base
ms.assetid: 379c236d-c6f5-4a12-8adc-aa6377e81e6c
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER, IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control, IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER control code, _win32_ioctl_storage_get_media_serial_number, base.ioctl_storage_get_media_serial_number, winioctl/IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
 - winioctl/IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER
---

# IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER IOCTL


## -description

Retrieves the serial number of a USB device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                         // handle to device
  IOCTL_STORAGE_GET_MEDIA_SERIAL_NUMBER,    // dwIoControlCode
  NULL,                                     // lpInBuffer
  0,                                        // nInBufferSize
  (LPVOID) lpOutBuffer,                     // output buffer
  (DWORD) nOutBufferSize,                   // size of output buffer
  (LPDWORD) lpBytesReturned,                // number of bytes returned
  (LPOVERLAPPED) lpOverlapped               // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -see-also

* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [MEDIA_SERIAL_NUMBER_DATA](/windows/desktop/DevIO/media-serial-number-data-str)