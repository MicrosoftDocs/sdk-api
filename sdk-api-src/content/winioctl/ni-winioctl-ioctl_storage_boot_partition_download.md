---
UID: NI:winioctl.IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
tech.root: fs
title: IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD
ms.date: 03/12/2026
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
      HANDLE hDevice,                 // handle to device
      IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD,  // dwIoControlCode
      LPVOID lpInBuffer,             // input buffer
      DWORD nInBufferSize,            // size of input buffer
      LPVOID lpOutBuffer,            // output buffer
      DWORD nOutBufferSize,           // size of output buffer
      LPDWORD lpBytesReturned,        // number of bytes returned
      LPOVERLAPPED lpOverlapped       // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

A pointer to a STORAGE_HW_BOOT_PARTITION_DOWNLOAD structure that specifies the boot partition image data to download, including the offset and size of the image chunk.

### -input-buffer-length

The size of the input buffer, in bytes. Set *nInBufferSize* to `sizeof(STORAGE_HW_BOOT_PARTITION_DOWNLOAD)` plus the size of the image data being transferred.

### -output-buffer

None. Set *lpOutBuffer* to **NULL**.

### -output-buffer-length

Set *nOutBufferSize* to zero.

### -status-block

If the operation completes successfully, [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) returns a nonzero value.

If the operation fails or is pending, [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) returns zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

This IOCTL transfers boot partition image data to the NVMe controller's internal buffer using the Firmware Download command. For large boot partition images that exceed the controller's transfer size limit, the image must be split into multiple chunks and downloaded using multiple IOCTL calls with appropriate offset values.

After all image data has been downloaded, use [IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE](ni-winioctl-ioctl_storage_boot_partition_activate.md) to commit the downloaded image to the boot partition.

The caller must have administrative privileges to issue this IOCTL.

## -see-also

[IOCTL_STORAGE_BOOT_PARTITION_GET_INFO IOCTL](ni-winioctl-ioctl_storage_boot_partition_get_info.md), [IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE IOCTL](ni-winioctl-ioctl_storage_boot_partition_activate.md)
