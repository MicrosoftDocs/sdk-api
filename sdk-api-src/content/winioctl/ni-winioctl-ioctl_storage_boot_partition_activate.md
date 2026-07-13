---
UID: NI:winioctl.IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE
tech.root: fs
title: IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE
ms.date: 02/25/2026
targetos: Windows
description: Activates or replaces a boot partition on the storage controller or disk using the NVMe Firmware Commit command (NVME_ADMIN_COMMAND_FIRMWARE_COMMIT) with boot partition-specific action codes.
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
 - IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE
f1_keywords:
 - IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE
 - winioctl/IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE
dev_langs:
 - c++
helpviewer_keywords:
 - IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE
---

# IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE IOCTL

## -description

Activates or replaces a boot partition on the storage controller or disk using the [NVMe Firmware Commit](../nvme/ne-nvme-nvme_admin_commands.md) command (NVME_ADMIN_COMMAND_FIRMWARE_COMMIT) with boot partition-specific action codes. This IOCTL supports two mutually exclusive operations: replacing an existing boot partition with a downloaded image or activating an existing boot partition.

To perform this operation, call the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
      (HANDLE) hDevice,                 // handle to device
      IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE,  // dwIoControlCode
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

A pointer to a [STORAGE_HW_BOOT_PARTITION_ACTIVATE](ns-winioctl-storage_hw_boot_partition_activate.md) structure that specifies the boot partition to activate and the action to perform.

### -input-buffer-length

The size of the input buffer, in bytes. Set *nInBufferSize* to `sizeof(STORAGE_BOOT_PARTITION_ACTIVATE)`.

### -output-buffer

None. Set *lpOutBuffer* to **NULL**.

### -output-buffer-length

Set *nOutBufferSize* to zero.

### -status-block

If the operation completes successfully, [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) returns a nonzero value.

If the operation fails or is pending, [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) returns zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

This IOCTL commits a boot partition image to the NVMe controller using the Firmware Commit command with boot partition-specific action codes. It supports two mutually exclusive operations:

- **Replace**: Commits a previously downloaded boot partition image (via [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md)) to the specified boot partition slot.
- **Activate**: Activates an existing boot partition without modifying its contents.

To update a boot partition, first use [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md) to transfer the image data, then use this IOCTL to commit and activate the new image.

The caller must have administrative privileges to issue this IOCTL.

## -see-also

[IOCTL_STORAGE_BOOT_PARTITION_GET_INFO IOCTL](ni-winioctl-ioctl_storage_boot_partition_get_info.md), [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD IOCTL](ni-winioctl-ioctl_storage_boot_partition_download.md)
