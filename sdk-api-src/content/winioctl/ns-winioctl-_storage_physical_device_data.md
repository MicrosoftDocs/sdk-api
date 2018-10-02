---
UID: NS:winioctl._STORAGE_PHYSICAL_DEVICE_DATA
title: "_STORAGE_PHYSICAL_DEVICE_DATA"
author: windows-sdk-content
description: Describes a physical storage device.
old-location: fs\storage_physical_device_data.htm
tech.root: fileio
ms.assetid: 4B484F79-DDC8-4671-90EA-D793EA0A05C7
ms.author: windowssdkdev
ms.date: 09/28/2018
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: STORAGE_PHYSICAL_DEVICE_DATA, *PSTORAGE_PHYSICAL_DEVICE_DATA
req.redist: 
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

A <a href="https://msdn.microsoft.com/ECC5A745-EA8B-4FBE-840D-0D959C9ED5BA">STORAGE_COMPONENT_HEALTH_STATUS</a> enumeration.


### -field CommandProtocol

A <a href="https://msdn.microsoft.com/8055B633-99EF-4AAE-AA80-FC09F357BEAB">STORAGE_PROTOCOL_TYPE</a> enumeration.


### -field SpecVersion

A <a href="https://msdn.microsoft.com/470DBBC0-A7D7-42A6-97D0-44AEAC990576">STORAGE_SPEC_VERSION</a> structure that specifies the supported storage spec version. For example: SBC 3, SATA 3.2, NVMe 1.2


### -field FormFactor

A <a href="https://msdn.microsoft.com/B8FCDC58-D599-4EEE-8096-818345FCD75F">STORAGE_DEVICE_FORM_FACTOR</a> enumeration.


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

