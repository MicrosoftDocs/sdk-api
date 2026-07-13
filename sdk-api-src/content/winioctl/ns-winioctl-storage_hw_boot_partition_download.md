---
UID: NS:winioctl._STORAGE_HW_BOOT_PARTITION_DOWNLOAD
tech.root: fs
title: STORAGE_HW_BOOT_PARTITION_DOWNLOAD
ms.date: 03/11/2026
targetos: Windows
description: Contains a boot partition image payload to be downloaded to an NVMe storage controller or disk.
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
req.typenames: STORAGE_HW_BOOT_PARTITION_DOWNLOAD, *PSTORAGE_HW_BOOT_PARTITION_DOWNLOAD
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
 - _STORAGE_HW_BOOT_PARTITION_DOWNLOAD
 - PSTORAGE_HW_BOOT_PARTITION_DOWNLOAD
 - STORAGE_HW_BOOT_PARTITION_DOWNLOAD
f1_keywords:
 - _STORAGE_HW_BOOT_PARTITION_DOWNLOAD
 - winioctl/_STORAGE_HW_BOOT_PARTITION_DOWNLOAD
 - PSTORAGE_HW_BOOT_PARTITION_DOWNLOAD
 - winioctl/PSTORAGE_HW_BOOT_PARTITION_DOWNLOAD
 - STORAGE_HW_BOOT_PARTITION_DOWNLOAD
 - winioctl/STORAGE_HW_BOOT_PARTITION_DOWNLOAD
dev_langs:
 - c++
helpviewer_keywords:
 - _STORAGE_HW_BOOT_PARTITION_DOWNLOAD
---

# STORAGE_HW_BOOT_PARTITION_DOWNLOAD structure

## -description

Contains a boot partition image payload to be downloaded to an NVMe storage controller or disk. This structure is used as the input buffer for the [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md) control code.

## -struct-fields

### -field Version

The version of this structure. Set this to **STORAGE_HW_BOOT_PARTITION_DOWNLOAD_STRUCTURE_VERSION** (0x01).

### -field Size

The size of this structure including the image buffer, in bytes.

### -field Flags

Flags associated with this download. The following are valid flags that this member can hold.

| Flag | Description |
| --- | --- |
| STORAGE_HW_BOOT_PARTITION_REQUEST_FLAG_CONTROLLER | Indicates that the target of the request is a controller or adapter, different than the device handle or object itself (for example, NVMe SSD or HBA). |

### -field BPID

The boot partition ID that the image will be downloaded to. Valid values are 0 or 1.

### -field Reserved[3]

Reserved for future use.

### -field Offset

The offset within the boot partition image where this chunk begins. This value should be aligned to **ImagePayloadAlignment** from [STORAGE_HW_BOOT_PARTITION_INFO](ns-winioctl-storage_hw_boot_partition_info.md).

### -field BufferSize

The size of the **ImageBuffer** data, in bytes. This value should be a multiple of **ImagePayloadAlignment** from [STORAGE_HW_BOOT_PARTITION_INFO](ns-winioctl-storage_hw_boot_partition_info.md).

### -field ImageBuffer[ANYSIZE_ARRAY]

The boot partition image data for this download chunk.

## -remarks

This structure is used with [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md), which issues an NVMe Firmware Download command (**NVME_ADMIN_COMMAND_FIRMWARE_IMAGE_DOWNLOAD**) to transfer image data to the controller's internal buffer. For large boot partition images that exceed the controller's maximum transfer size (reported in **ImagePayloadMaxSize** from [STORAGE_HW_BOOT_PARTITION_INFO](ns-winioctl-storage_hw_boot_partition_info.md)), the image must be split into multiple chunks and downloaded using multiple IOCTL calls with the appropriate **Offset** values.

After all image data has been downloaded, use [IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE](ni-winioctl-ioctl_storage_boot_partition_activate.md) with the **STORAGE_HW_BOOT_PARTITION_REQUEST_REPLACE_EXISTING_BOOT_PARTITION** flag to commit the downloaded image to the boot partition.

> [!NOTE]
> These IOCTLs are currently only supported for PCIe NVMe devices.

## -see-also

[IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md)

[IOCTL_STORAGE_BOOT_PARTITION_GET_INFO](ni-winioctl-ioctl_storage_boot_partition_get_info.md)

[IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE](ni-winioctl-ioctl_storage_boot_partition_activate.md)

[STORAGE_HW_BOOT_PARTITION_INFO](ns-winioctl-storage_hw_boot_partition_info.md)

[STORAGE_HW_BOOT_PARTITION_ACTIVATE](ns-winioctl-storage_hw_boot_partition_activate.md)

