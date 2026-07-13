---
UID: NI:winioctl.IOCTL_STORAGE_READ_CAPACITY
title: IOCTL_STORAGE_READ_CAPACITY
description: Retrieves the geometry information for the device. (IOCTL_STORAGE_READ_CAPACITY)
helpviewer_keywords: ["IOCTL_STORAGE_READ_CAPACITY","IOCTL_STORAGE_READ_CAPACITY control","IOCTL_STORAGE_READ_CAPACITY control code","base.ioctl_storage_read_capacity","winioctl/IOCTL_STORAGE_READ_CAPACITY"]
old-location: base\ioctl_storage_read_capacity.htm
tech.root: base
ms.assetid: c0a2c73c-fae9-40e9-8009-4dffbb03a01d
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_READ_CAPACITY, IOCTL_STORAGE_READ_CAPACITY control, IOCTL_STORAGE_READ_CAPACITY control code, base.ioctl_storage_read_capacity, winioctl/IOCTL_STORAGE_READ_CAPACITY
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
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
 - IOCTL_STORAGE_READ_CAPACITY
 - winioctl/IOCTL_STORAGE_READ_CAPACITY
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
 - IOCTL_STORAGE_READ_CAPACITY
---

# IOCTL_STORAGE_READ_CAPACITY IOCTL


## -description

Retrieves the geometry information for the device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_STORAGE_READ_CAPACITY,  // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure 
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
* [STORAGE_READ_CAPACITY](/windows/desktop/DevIO/storage-read-capacity)
