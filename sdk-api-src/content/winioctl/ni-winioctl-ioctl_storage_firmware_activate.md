---
UID: NI:winioctl.IOCTL_STORAGE_FIRMWARE_ACTIVATE
title: IOCTL_STORAGE_FIRMWARE_ACTIVATE
description: Windows applications can use this control code to activate a firmware image on a specified device.
helpviewer_keywords: ["IOCTL_STORAGE_FIRMWARE_ACTIVATE","IOCTL_STORAGE_FIRMWARE_ACTIVATE control","IOCTL_STORAGE_FIRMWARE_ACTIVATE control code [Files]","fs.ioctl_storage_firmware_activate","winioctl/IOCTL_STORAGE_FIRMWARE_ACTIVATE"]
old-location: fs\ioctl_storage_firmware_activate.htm
tech.root: fs
ms.assetid: 000BEB58-D91E-4859-AC31-A4C72B84A982
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_FIRMWARE_ACTIVATE, IOCTL_STORAGE_FIRMWARE_ACTIVATE control, IOCTL_STORAGE_FIRMWARE_ACTIVATE control code [Files], fs.ioctl_storage_firmware_activate, winioctl/IOCTL_STORAGE_FIRMWARE_ACTIVATE
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IOCTL_STORAGE_FIRMWARE_ACTIVATE
 - winioctl/IOCTL_STORAGE_FIRMWARE_ACTIVATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - IOCTL_STORAGE_FIRMWARE_ACTIVATE
---

# IOCTL_STORAGE_FIRMWARE_ACTIVATE IOCTL


## -description

Windows applications can use this control code to activate a firmware image on a specified device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_FIRMWARE_ACTIVATE,  // dwIoControlCode
  (LPDWORD) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
  (LPDWORD) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [IOCTL_STORAGE_FIRMWARE_DOWNLOAD](ni-winioctl-ioctl_storage_firmware_download.md)
* [IOCTL_STORAGE_FIRMWARE_GET_INFO](ni-winioctl-ioctl_storage_firmware_get_info.md)
* [STORAGE_HW_FIRMWARE_ACTIVATE](ns-winioctl-storage_hw_firmware_activate.md)
* [STORAGE_HW_FIRMWARE_DOWNLOAD](ns-winioctl-storage_hw_firmware_download.md)
* [STORAGE_HW_FIRMWARE_INFO](/windows/desktop/FileIO/storage-hw-firmware-info)
* [STORAGE_HW_FIRMWARE_INFO_QUERY](/windows/desktop/FileIO/storage-hw-firmware-info-query)
* [STORAGE_HW_FIRMWARE_SLOT_INFO](/windows/desktop/FileIO/storage-hw-firmware-slot-info)