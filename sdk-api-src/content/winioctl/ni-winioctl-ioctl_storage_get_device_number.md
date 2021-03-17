---
UID: NI:winioctl.IOCTL_STORAGE_GET_DEVICE_NUMBER
title: IOCTL_STORAGE_GET_DEVICE_NUMBER
description: Retrieves the device type, device number, and, for a partitionable device, the partition number of a device.
helpviewer_keywords: ["IOCTL_STORAGE_GET_DEVICE_NUMBER","IOCTL_STORAGE_GET_DEVICE_NUMBER control","IOCTL_STORAGE_GET_DEVICE_NUMBER control code","base.ioctl_storage_get_device_number","winioctl/IOCTL_STORAGE_GET_DEVICE_NUMBER"]
old-location: base\ioctl_storage_get_device_number.htm
tech.root: base
ms.assetid: 2cd9610b-aa83-4d0a-a7a9-1d4dab8be331
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_DEVICE_NUMBER, IOCTL_STORAGE_GET_DEVICE_NUMBER control, IOCTL_STORAGE_GET_DEVICE_NUMBER control code, base.ioctl_storage_get_device_number, winioctl/IOCTL_STORAGE_GET_DEVICE_NUMBER
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
 - IOCTL_STORAGE_GET_DEVICE_NUMBER
 - winioctl/IOCTL_STORAGE_GET_DEVICE_NUMBER
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
 - IOCTL_STORAGE_GET_DEVICE_NUMBER
---

# IOCTL_STORAGE_GET_DEVICE_NUMBER IOCTL


## -description

Retrieves the device type, device number, and, for a partitionable device, the partition number of a device. 

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_GET_DEVICE_NUMBER,  // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID), lpOutBuffer,            // output buffer
  (DWORD), nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
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

## -remarks

The values in the [STORAGE_DEVICE_NUMBER](ns-winioctl-storage_device_number.md) structure are guaranteed to remain unchanged until the device is removed or the system is restarted. It is not guaranteed to be persistent across device restarts or system restarts.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [STORAGE_DEVICE_NUMBER](ns-winioctl-storage_device_number.md)