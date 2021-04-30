---
UID: NS:winioctl._STORAGE_PHYSICAL_DEVICE_DATA
title: STORAGE_PHYSICAL_DEVICE_DATA
description: Describes a physical storage device.
helpviewer_keywords: ["*PSTORAGE_PHYSICAL_DEVICE_DATA","PSTORAGE_PHYSICAL_DEVICE_DATA","PSTORAGE_PHYSICAL_DEVICE_DATA structure pointer [Files]","STORAGE_PHYSICAL_DEVICE_DATA","STORAGE_PHYSICAL_DEVICE_DATA structure [Files]","fs.storage_physical_device_data","winioctl/PSTORAGE_PHYSICAL_DEVICE_DATA","winioctl/_STORAGE_PHYSICAL_DEVICE_DATA"]
old-location: fs\storage_physical_device_data.htm
tech.root: fs
ms.assetid: 4B484F79-DDC8-4671-90EA-D793EA0A05C7
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PHYSICAL_DEVICE_DATA, PSTORAGE_PHYSICAL_DEVICE_DATA, PSTORAGE_PHYSICAL_DEVICE_DATA structure pointer [Files], STORAGE_PHYSICAL_DEVICE_DATA, STORAGE_PHYSICAL_DEVICE_DATA structure [Files], fs.storage_physical_device_data, winioctl/PSTORAGE_PHYSICAL_DEVICE_DATA, winioctl/_STORAGE_PHYSICAL_DEVICE_DATA'
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
req.typenames: STORAGE_PHYSICAL_DEVICE_DATA, *PSTORAGE_PHYSICAL_DEVICE_DATA
req.redist: 
f1_keywords:
 - _STORAGE_PHYSICAL_DEVICE_DATA
 - winioctl/_STORAGE_PHYSICAL_DEVICE_DATA
 - PSTORAGE_PHYSICAL_DEVICE_DATA
 - winioctl/PSTORAGE_PHYSICAL_DEVICE_DATA
 - STORAGE_PHYSICAL_DEVICE_DATA
 - winioctl/STORAGE_PHYSICAL_DEVICE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_PHYSICAL_DEVICE_DATA
---

# STORAGE_PHYSICAL_DEVICE_DATA structure


## -description

Describes a physical storage device.

## -struct-fields

### -field DeviceId

Specifies the device ID.

### -field Role

Value(s) of bitmask from STORAGE_COMPONENT_ROLE_xxx

### -field HealthStatus

A <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_component_health_status">STORAGE_COMPONENT_HEALTH_STATUS</a> enumeration.

### -field CommandProtocol

A <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_protocol_type">STORAGE_PROTOCOL_TYPE</a> enumeration.

### -field SpecVersion

A <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_spec_version">STORAGE_SPEC_VERSION</a> structure that specifies the supported storage spec version. For example: SBC 3, SATA 3.2, NVMe 1.2

### -field FormFactor

A <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_device_form_factor">STORAGE_DEVICE_FORM_FACTOR</a> enumeration.

### -field Vendor

Specifies the device vendor.

### -field Model

Specifies the device model.

### -field FirmwareRevision

Specifies the firmware revision of the device.

### -field Capacity

In units of kilobytes (1024 bytes).

### -field PhysicalLocation

Reserved for future use.

### -field Reserved