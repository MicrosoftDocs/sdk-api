---
UID: NI:winioctl.IOCTL_STORAGE_FIRMWARE_DOWNLOAD
title: IOCTL_STORAGE_FIRMWARE_DOWNLOAD
description: Windows applications can use this control code to download a firmware image to the target device, but not activate it.
helpviewer_keywords: ["IOCTL_STORAGE_FIRMWARE_DOWNLOAD","IOCTL_STORAGE_FIRMWARE_DOWNLOAD control","IOCTL_STORAGE_FIRMWARE_DOWNLOAD control code [Files]","fs.ioctl_storage_firmware_download","winioctl/IOCTL_STORAGE_FIRMWARE_DOWNLOAD"]
old-location: fs\ioctl_storage_firmware_download.htm
tech.root: fs
ms.assetid: 77E50787-1E71-4D90-A1D3-E6665CE0EFDC
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_FIRMWARE_DOWNLOAD, IOCTL_STORAGE_FIRMWARE_DOWNLOAD control, IOCTL_STORAGE_FIRMWARE_DOWNLOAD control code [Files], fs.ioctl_storage_firmware_download, winioctl/IOCTL_STORAGE_FIRMWARE_DOWNLOAD
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
 - IOCTL_STORAGE_FIRMWARE_DOWNLOAD
 - winioctl/IOCTL_STORAGE_FIRMWARE_DOWNLOAD
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
 - IOCTL_STORAGE_FIRMWARE_DOWNLOAD
---

# IOCTL_STORAGE_FIRMWARE_DOWNLOAD IOCTL


## -description

Windows applications can use this control code to download a firmware image to the target device, but not activate it. If the image to be downloaded is larger than the controller’s maximum data transfer size, this IOCTL will have to be called multiple times until the entire image is downloaded.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_FIRMWARE_DOWNLOAD,  // dwIoControlCode
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
* [IOCTL_STORAGE_FIRMWARE_ACTIVATE](ni-winioctl-ioctl_storage_firmware_activate.md)
* [IOCTL_STORAGE_FIRMWARE_GET_INFO](ni-winioctl-ioctl_storage_firmware_get_info.md)
* [STORAGE_HW_FIRMWARE_ACTIVATE](ns-winioctl-storage_hw_firmware_activate.md)
* [STORAGE_HW_FIRMWARE_DOWNLOAD](ns-winioctl-storage_hw_firmware_download.md)
* [STORAGE_HW_FIRMWARE_INFO](/windows/desktop/FileIO/storage-hw-firmware-info)
* [STORAGE_HW_FIRMWARE_INFO_QUERY](/windows/desktop/FileIO/storage-hw-firmware-info-query)
* [STORAGE_HW_FIRMWARE_SLOT_INFO](/windows/desktop/FileIO/storage-hw-firmware-slot-info)