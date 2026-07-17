---
UID: NS:winioctl._STORAGE_HW_BOOT_PARTITION_INFO
tech.root: fs
title: STORAGE_HW_BOOT_PARTITION_INFO
ms.date: 03/11/2026
targetos: Windows
description: Contains boot partition information retrieved from an NVMe storage controller or disk.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winioctl.h
req.include-header: Windows.h
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 26H1
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: STORAGE_HW_BOOT_PARTITION_INFO, *PSTORAGE_HW_BOOT_PARTITION_INFO
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - _STORAGE_HW_BOOT_PARTITION_INFO
 - PSTORAGE_HW_BOOT_PARTITION_INFO
 - STORAGE_HW_BOOT_PARTITION_INFO
f1_keywords:
 - _STORAGE_HW_BOOT_PARTITION_INFO
 - winioctl/_STORAGE_HW_BOOT_PARTITION_INFO
 - PSTORAGE_HW_BOOT_PARTITION_INFO
 - winioctl/PSTORAGE_HW_BOOT_PARTITION_INFO
 - STORAGE_HW_BOOT_PARTITION_INFO
 - winioctl/STORAGE_HW_BOOT_PARTITION_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - _STORAGE_HW_BOOT_PARTITION_INFO
---

# STORAGE_HW_BOOT_PARTITION_INFO structure

## -description

Contains boot partition information retrieved from an NVMe storage controller or disk. This structure is used as the input and output buffer for the [IOCTL_STORAGE_BOOT_PARTITION_GET_INFO](ni-winioctl-ioctl_storage_boot_partition_get_info.md) control code.

## -struct-fields

### -field Version

The version of this structure. Set this to **STORAGE_HW_BOOT_PARTITION_INFO_STRUCTURE_VERSION_V1** (0x01).

### -field Size

The size of this structure, in bytes.

### -field BPSZ

The boot partition size, in bytes.

### -field Flags

Flags associated with this request. The following are valid flags that this member can hold.

| Flag | Description |
| --- | --- |
| STORAGE_HW_BOOT_PARTITION_REQUEST_FLAG_CONTROLLER | Indicates that the target of the request is a controller or adapter, different than the device handle or object itself (for example, NVMe SSD or HBA). |

### -field ImagePayloadAlignment

The alignment of the image payload, in bytes. The maximum value is **PAGE_SIZE**. The transfer size must be a multiple of this value. Some protocols require at least sector-size alignment. A value of 0 indicates that the alignment value is invalid or not applicable.

### -field ImagePayloadMaxSize

The maximum size for a single image payload command, in bytes.

### -field SlotCount

The number of boot partition slots available. For NVMe devices, this value is 2 as defined by the NVMe specification.

### -field ABPID

The active boot partition ID (0 or 1).

## -remarks

This structure is returned by [IOCTL_STORAGE_BOOT_PARTITION_GET_INFO](ni-winioctl-ioctl_storage_boot_partition_get_info.md), which issues a Get Log Page command for the Boot Partition Log Page (**NVME_LOG_PAGE_BOOT_PARTITION**) to retrieve boot partition state from the NVMe controller.

The **ImagePayloadAlignment** and **ImagePayloadMaxSize** values should be used when preparing image data for download via [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md). The download buffer offset must be aligned to **ImagePayloadAlignment**, and each chunk size should be a multiple of **ImagePayloadAlignment** and not exceed **ImagePayloadMaxSize**.

> [!NOTE]
> These IOCTLs are currently only supported for PCIe NVMe devices.

## -see-also

[IOCTL_STORAGE_BOOT_PARTITION_GET_INFO](ni-winioctl-ioctl_storage_boot_partition_get_info.md)

[IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md)

[IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE](ni-winioctl-ioctl_storage_boot_partition_activate.md)

[STORAGE_HW_BOOT_PARTITION_DOWNLOAD](ns-winioctl-storage_hw_boot_partition_download.md)

[STORAGE_HW_BOOT_PARTITION_ACTIVATE](ns-winioctl-storage_hw_boot_partition_activate.md)

