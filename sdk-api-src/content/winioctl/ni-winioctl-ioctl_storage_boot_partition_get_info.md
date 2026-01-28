---
UID: NI:winioctl.IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
tech.root: fs
title: IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
ms.date: 01/23/2026
targetos: Windows
description: Retrieves boot partition information from a storage controller or disk by issuing a GetLogPage command for the Boot Partition Log Page (NVME_LOG_PAGE_BOOT_PARTITION).
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
 - IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
f1_keywords:
 - IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
 - winioctl/IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
---

# IOCTL_STORAGE_BOOT_PARTITION_GET_INFO IOCTL

## -description

Retrieves boot partition information from a storage controller or disk by issuing a [GetLogPage](../nvme/ns-nvme-nvme_command.md) command for the **Boot Partition Log Page** (NVME_LOG_PAGE_BOOT_PARTITION).

To perform this operation, call the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                             // handle to file
  IOCTL_STORAGE_BOOT_PARTITION_GET_INFO,        // dwIoControlCode
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

[IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE IOCTL](ni-winioctl-ioctl_storage_boot_partition_activate.md), [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD IOCTL](ni-winioctl-ioctl_storage_boot_partition_download.md)
