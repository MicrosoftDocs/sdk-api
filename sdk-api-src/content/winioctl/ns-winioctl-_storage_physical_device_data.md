---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

