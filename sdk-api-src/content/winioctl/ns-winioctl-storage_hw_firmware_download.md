---
UID: NS:winioctl._STORAGE_HW_FIRMWARE_DOWNLOAD
title: STORAGE_HW_FIRMWARE_DOWNLOAD
description: This structure contains a firmware image payload to be downloaded to the target.
helpviewer_keywords: ["*PSTORAGE_HW_FIRMWARE_DOWNLOAD","PSTORAGE_HW_FIRMWARE_DOWNLOAD","PSTORAGE_HW_FIRMWARE_DOWNLOAD structure pointer [Files]","STORAGE_HW_FIRMWARE_DOWNLOAD","STORAGE_HW_FIRMWARE_DOWNLOAD structure [Files]","fs.storage_hw_firmware_download","winioctl/PSTORAGE_HW_FIRMWARE_DOWNLOAD","winioctl/STORAGE_HW_FIRMWARE_DOWNLOAD"]
old-location: fs\storage_hw_firmware_download.htm
tech.root: fs
ms.assetid: BD1D39C7-9624-400C-BF4D-5F7583AA82FB
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_HW_FIRMWARE_DOWNLOAD, PSTORAGE_HW_FIRMWARE_DOWNLOAD, PSTORAGE_HW_FIRMWARE_DOWNLOAD structure pointer [Files], STORAGE_HW_FIRMWARE_DOWNLOAD, STORAGE_HW_FIRMWARE_DOWNLOAD structure [Files], fs.storage_hw_firmware_download, winioctl/PSTORAGE_HW_FIRMWARE_DOWNLOAD, winioctl/STORAGE_HW_FIRMWARE_DOWNLOAD'
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
req.typenames: STORAGE_HW_FIRMWARE_DOWNLOAD, *PSTORAGE_HW_FIRMWARE_DOWNLOAD
req.redist: 
f1_keywords:
 - _STORAGE_HW_FIRMWARE_DOWNLOAD
 - winioctl/_STORAGE_HW_FIRMWARE_DOWNLOAD
 - PSTORAGE_HW_FIRMWARE_DOWNLOAD
 - winioctl/PSTORAGE_HW_FIRMWARE_DOWNLOAD
 - STORAGE_HW_FIRMWARE_DOWNLOAD
 - winioctl/STORAGE_HW_FIRMWARE_DOWNLOAD
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
 - STORAGE_HW_FIRMWARE_DOWNLOAD
---

# STORAGE_HW_FIRMWARE_DOWNLOAD structure


## -description

This structure contains a  firmware image payload to be downloaded to the target.

## -struct-fields

### -field Version

The version of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_DOWNLOAD).

### -field Size

The size of this structure and the download image buffer.

### -field Flags

Flags associated with this download. The following are valid flags that this member can hold.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_CONTROLLER</td>
<td>Indicates that the target of the request is a controller or adapter, different than the device handler or object itself (e.g. NVMe SSD or HBA).</td>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_LAST_SEGMENT</td>
<td>Indicates that the current firmware image segment is the last one.</td>
</tr>
</table>

### -field Slot

The slot number that the firmware image will be downloaded to.

### -field Reserved

Reserved for future use.

### -field Offset

The offset in this buffer of where the Image file begins. This should be aligned to <b>ImagePayloadAlignment</b> from <a href="/windows/desktop/FileIO/storage-hw-firmware-info">STORAGE_HW_FIRMWARE_INFO</a>.

### -field BufferSize

The buffer size of the ImageBuffer. This should be a multiple of <b>ImagePayloadAlignment</b> from <a href="/windows/desktop/FileIO/storage-hw-firmware-info">STORAGE_HW_FIRMWARE_INFO</a>.

### -field ImageBuffer

The firmware image file.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_activate">IOCTL_STORAGE_FIRMWARE_ACTIVATE</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_download">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_firmware_get_info">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate">STORAGE_HW_FIRMWARE_ACTIVATE</a>



<a href="/windows/desktop/FileIO/storage-hw-firmware-info">STORAGE_HW_FIRMWARE_INFO</a>



<a href="/windows/desktop/FileIO/storage-hw-firmware-info-query">STORAGE_HW_FIRMWARE_INFO_QUERY</a>



<a href="/windows/desktop/FileIO/storage-hw-firmware-slot-info">STORAGE_HW_FIRMWARE_SLOT_INFO</a>