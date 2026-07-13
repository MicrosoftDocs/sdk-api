---
UID: NI:winioctl.IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
tech.root: fs
title: IOCTL_STORAGE_BOOT_PARTITION_GET_INFO
ms.date: 03/13/2026
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
    HANDLE hDevice,                   // handle to device
    IOCTL_STORAGE_BOOT_PARTITION_GET_INFO,  // dwIoControlCode
    LPVOID lpInBuffer,                // input buffer
    DWORD nInBufferSize,              // size of input buffer
    LPVOID lpOutBuffer,               // output buffer
    DWORD nOutBufferSize,             // size of output buffer
    LPDWORD lpBytesReturned,          // number of bytes returned
    LPOVERLAPPED lpOverlapped         // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

A pointer to a [STORAGE_HW_BOOT_PARTITION_INFO](ns-winioctl-storage_hw_boot_partition_info.md) structure. Set *nInBufferSize* to `sizeof(STORAGE_HW_BOOT_PARTITION_INFO)`.

### -input-buffer-length

The size of the input buffer, in bytes.

### -output-buffer

A pointer to a [STORAGE_HW_BOOT_PARTITION_INFO](ns-winioctl-storage_hw_boot_partition_info.md) structure that receives the boot partition information. Set *nOutBufferSize* to `sizeof(STORAGE_HW_BOOT_PARTITION_INFO)`.

### -output-buffer-length

The size of the output buffer, in bytes.

### -status-block

If the operation completes successfully, [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) returns a nonzero value.

If the operation fails or is pending, [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) returns zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

This IOCTL is used to query boot partition information from NVMe storage devices that support boot partitions. The controller issues a GetLogPage command requesting the Boot Partition Log Page (NVME_LOG_PAGE_BOOT_PARTITION) to retrieve this information.

The caller must have administrative privileges to issue this IOCTL.

## -see-also

[IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE IOCTL](ni-winioctl-ioctl_storage_boot_partition_activate.md), [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD IOCTL](ni-winioctl-ioctl_storage_boot_partition_download.md)
