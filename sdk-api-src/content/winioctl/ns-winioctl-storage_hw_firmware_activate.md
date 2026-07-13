---
UID: NS:winioctl._STORAGE_HW_FIRMWARE_ACTIVATE
title: STORAGE_HW_FIRMWARE_ACTIVATE
description: This structure contains information about the downloaded firmware to activate.
helpviewer_keywords: ["*PSTORAGE_HW_FIRMWARE_ACTIVATE","PSTORAGE_HW_FIRMWARE_ACTIVATE","PSTORAGE_HW_FIRMWARE_ACTIVATE structure pointer [Files]","STORAGE_HW_FIRMWARE_ACTIVATE","STORAGE_HW_FIRMWARE_ACTIVATE structure [Files]","fs.storage_hw_firmware_activate","winioctl/PSTORAGE_HW_FIRMWARE_ACTIVATE","winioctl/STORAGE_HW_FIRMWARE_ACTIVATE"]
old-location: fs\storage_hw_firmware_activate.htm
tech.root: fs
ms.assetid: 2DAAC1FE-2503-4820-9718-9A653B0A05CA
ms.date: 11/18/2024
ms.keywords: '*PSTORAGE_HW_FIRMWARE_ACTIVATE, PSTORAGE_HW_FIRMWARE_ACTIVATE, PSTORAGE_HW_FIRMWARE_ACTIVATE structure pointer [Files], STORAGE_HW_FIRMWARE_ACTIVATE, STORAGE_HW_FIRMWARE_ACTIVATE structure [Files], fs.storage_hw_firmware_activate, winioctl/PSTORAGE_HW_FIRMWARE_ACTIVATE, winioctl/STORAGE_HW_FIRMWARE_ACTIVATE'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: STORAGE_HW_FIRMWARE_ACTIVATE, *PSTORAGE_HW_FIRMWARE_ACTIVATE
req.redist: 
f1_keywords:
 - _STORAGE_HW_FIRMWARE_ACTIVATE
 - winioctl/_STORAGE_HW_FIRMWARE_ACTIVATE
 - PSTORAGE_HW_FIRMWARE_ACTIVATE
 - winioctl/PSTORAGE_HW_FIRMWARE_ACTIVATE
 - STORAGE_HW_FIRMWARE_ACTIVATE
 - winioctl/STORAGE_HW_FIRMWARE_ACTIVATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - STORAGE_HW_FIRMWARE_ACTIVATE
---

# STORAGE_HW_FIRMWARE_ACTIVATE structure


## -description

This structure contains information about the downloaded firmware to activate.

## -struct-fields

### -field Version

The version of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_ACTIVATE).

### -field Size

The size of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_ACTIVATE).

### -field Flags

The flags associated with the activation request. The following are valid flags that can be set in this member.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_CONTROLLER</td>
<td>Indicates that the target of the request is a controller or adapter, different than the device handle or object itself (e.g. NVMe SSD or HBA).</td>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_SWITCH_TO_EXISTING_FIRMWARE</td>
<td>Indicates that the existing firmware image in the specified slot should be activated.</td>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_REPLACE_EXISTING_IMAGE</td>
<td><strong>Supported in Windows 11, version 24H2, and later.</strong><br>Indicates that the existing firmware in the slot should be activated with a controller reset.</td>
</tr>
</table>

### -field Slot

The slot with the firmware image that is to be activated.

### -field Reserved0

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_activate">IOCTL_STORAGE_FIRMWARE_ACTIVATE</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_download">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_get_info">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="/windows/desktop/FileIO/storage-hw-firmware-info">STORAGE_HW_FIRMWARE_INFO</a>



<a href="/windows/desktop/FileIO/storage-hw-firmware-info-query">STORAGE_HW_FIRMWARE_INFO_QUERY</a>



<a href="/windows/desktop/FileIO/storage-hw-firmware-slot-info">STORAGE_HW_FIRMWARE_SLOT_INFO</a>