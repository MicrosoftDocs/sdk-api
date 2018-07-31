---
UID: NS:winioctl._STORAGE_PHYSICAL_DEVICE_DATA
title: "_STORAGE_PHYSICAL_DEVICE_DATA"
author: windows-sdk-content
description: Describes a physical storage device.
old-location: fs\storage_physical_device_data.htm
old-project: FileIO
ms.assetid: 4B484F79-DDC8-4671-90EA-D793EA0A05C7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PSTORAGE_PHYSICAL_DEVICE_DATA, PSTORAGE_PHYSICAL_DEVICE_DATA, PSTORAGE_PHYSICAL_DEVICE_DATA structure pointer [Files], STORAGE_PHYSICAL_DEVICE_DATA, STORAGE_PHYSICAL_DEVICE_DATA structure [Files], _STORAGE_PHYSICAL_DEVICE_DATA, fs.storage_physical_device_data, winioctl/PSTORAGE_PHYSICAL_DEVICE_DATA, winioctl/_STORAGE_PHYSICAL_DEVICE_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: STORAGE_PHYSICAL_DEVICE_DATA, *PSTORAGE_PHYSICAL_DEVICE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_PHYSICAL_DEVICE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_PHYSICAL_DEVICE_DATA structure


## -description


Describes a physical storage device.


## -struct-fields




### -field DeviceId

Specifies the device ID.


### -field Role

Value(s) of bitmask from STORAGE_COMPONENT_ROLE_xxx


### -field HealthStatus

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt653957">STORAGE_COMPONENT_HEALTH_STATUS</a> enumeration.


### -field CommandProtocol

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn931818">STORAGE_PROTOCOL_TYPE</a> enumeration.


### -field SpecVersion

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt653963">STORAGE_SPEC_VERSION</a> structure that specifies the supported storage spec version. For example: SBC 3, SATA 3.2, NVMe 1.2


### -field FormFactor

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt653958">STORAGE_DEVICE_FORM_FACTOR</a> enumeration.


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

