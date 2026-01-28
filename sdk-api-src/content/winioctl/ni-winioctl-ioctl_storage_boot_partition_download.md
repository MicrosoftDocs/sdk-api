---
UID: NI:winioctl.IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
tech.root: fs
title: IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
ms.date: 01/26/2026
targetos: Windows
description: Downloads a boot partition image to the storage controller or disk using the NVMe Firmware Download command (NVME_ADMIN_COMMAND_FIRMWARE_IMAGE_DOWNLOAD) opcode to transfer image data to the controller's internal buffer.
prerelease: false
req.construct-type: ioctl
req.ddi-compliance: 
req.dll: 
req.header: winioctl.h
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 26H1
req.target-min-winversvr:
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
f1_keywords:
 - IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
 - winioctl/IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
dev_langs:
 - c++
helpviewer_keywords:
 - IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
---

# IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD IOCTL

## -description

Downloads a boot partition image to the storage controller or disk using the [NVMe Firmware Download](../nvme/ne-nvme-nvme_admin_commands.md) command (NVME_ADMIN_COMMAND_FIRMWARE_IMAGE_DOWNLOAD) opcode to transfer image data to the controller's internal buffer. Multiple download requests may be required for large images (using offset-based chunking).

To perform this operation, call the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                             // handle to file
  IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD,        // dwIoControlCode
  NULL,                                         // lpInBuffer
  0,                                            // nInBufferSize
  NULL,                                         // lpOutBuffer
  0,                                            // nOutBufferSize
  (LPDWORD) lpBytesReturned,                    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped                   // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

## -remarks

## -see-also

[IOCTL_STORAGE_BOOT_PARTITION_GET_INFO IOCTL](ni-winioctl-ioctl_storage_boot_partition_get_info.md), [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD IOCTL](ni-winioctl-ioctl_storage_boot_partition_download.md)
