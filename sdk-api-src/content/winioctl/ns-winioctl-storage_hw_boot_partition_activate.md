---
UID: NS:winioctl._STORAGE_HW_BOOT_PARTITION_ACTIVATE
tech.root: fs
title: STORAGE_HW_BOOT_PARTITION_ACTIVATE
ms.date: 03/11/2026
targetos: Windows
description: Contains information about the boot partition to activate or replace on an NVMe storage controller or disk.
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
req.typenames: STORAGE_HW_BOOT_PARTITION_ACTIVATE, *PSTORAGE_HW_BOOT_PARTITION_ACTIVATE
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
 - _STORAGE_HW_BOOT_PARTITION_ACTIVATE
 - PSTORAGE_HW_BOOT_PARTITION_ACTIVATE
 - STORAGE_HW_BOOT_PARTITION_ACTIVATE
f1_keywords:
 - _STORAGE_HW_BOOT_PARTITION_ACTIVATE
 - winioctl/_STORAGE_HW_BOOT_PARTITION_ACTIVATE
 - PSTORAGE_HW_BOOT_PARTITION_ACTIVATE
 - winioctl/PSTORAGE_HW_BOOT_PARTITION_ACTIVATE
 - STORAGE_HW_BOOT_PARTITION_ACTIVATE
 - winioctl/STORAGE_HW_BOOT_PARTITION_ACTIVATE
dev_langs:
 - c++
helpviewer_keywords:
 - _STORAGE_HW_BOOT_PARTITION_ACTIVATE
---

# STORAGE_HW_BOOT_PARTITION_ACTIVATE structure

## -description

Contains information about the boot partition to activate or replace on an NVMe storage controller or disk. This structure is used as the input buffer for the [IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE](ni-winioctl-ioctl_storage_boot_partition_activate.md) control code.

## -struct-fields

### -field Version

The version of this structure. Set this to **STORAGE_HW_BOOT_PARTITION_ACTIVATE_STRUCTURE_VERSION** (0x01).

### -field Size

The size of this structure, in bytes. Set this to `sizeof(STORAGE_HW_BOOT_PARTITION_ACTIVATE)`.

### -field Flags

Flags associated with this activation request. The following are valid flags that this member can hold. Only one action flag (**STORAGE_HW_BOOT_PARTITION_REQUEST_REPLACE_EXISTING_BOOT_PARTITION** or **STORAGE_HW_BOOT_PARTITION_REQUEST_ACTIVATE_EXISTING_BOOT_PARTITION**) may be set.

| Flag | Description |
|---|---|
| STORAGE_HW_BOOT_PARTITION_REQUEST_FLAG_CONTROLLER | Indicates that the target of the request is a controller or adapter, different than the device handle or object itself (for example, NVMe SSD or HBA). |
| STORAGE_HW_BOOT_PARTITION_REQUEST_REPLACE_EXISTING_BOOT_PARTITION | Replace the boot partition with the previously downloaded image. This corresponds to NVMe Firmware Commit Action 6. |
| STORAGE_HW_BOOT_PARTITION_REQUEST_ACTIVATE_EXISTING_BOOT_PARTITION | Activate an existing boot partition without modifying its contents. This corresponds to NVMe Firmware Commit Action 7. |

### -field BPID

The boot partition ID to activate. Valid values are 0 or 1.

### -field Reserved[3]

Reserved for future use.

## -remarks

This structure is used with [IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE](ni-winioctl-ioctl_storage_boot_partition_activate.md), which issues an NVMe Firmware Commit command (**NVME_ADMIN_COMMAND_FIRMWARE_COMMIT**) with boot partition-specific action codes. The IOCTL supports two mutually exclusive operations:

- **Replace** (Action 6): Commits a previously downloaded boot partition image (via [IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md)) to the specified boot partition slot. Set the **STORAGE_HW_BOOT_PARTITION_REQUEST_REPLACE_EXISTING_BOOT_PARTITION** flag.
- **Activate** (Action 7): Activates an existing boot partition without modifying its contents. Set the **STORAGE_HW_BOOT_PARTITION_REQUEST_ACTIVATE_EXISTING_BOOT_PARTITION** flag.

> [!NOTE]
> These IOCTLs are currently only supported for PCIe NVMe devices.

## -see-also

[IOCTL_STORAGE_BOOT_PARTITION_ACTIVATE](ni-winioctl-ioctl_storage_boot_partition_activate.md)

[IOCTL_STORAGE_BOOT_PARTITION_DOWNLOAD](ni-winioctl-ioctl_storage_boot_partition_download.md)

[IOCTL_STORAGE_BOOT_PARTITION_GET_INFO](ni-winioctl-ioctl_storage_boot_partition_get_info.md)

[STORAGE_HW_BOOT_PARTITION_INFO](ns-winioctl-storage_hw_boot_partition_info.md)

[STORAGE_HW_BOOT_PARTITION_DOWNLOAD](ns-winioctl-storage_hw_boot_partition_download.md)

