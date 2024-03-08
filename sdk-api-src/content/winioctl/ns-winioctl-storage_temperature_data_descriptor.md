---
UID: NS:winioctl._STORAGE_TEMPERATURE_DATA_DESCRIPTOR
title: STORAGE_TEMPERATURE_DATA_DESCRIPTOR
description: This structure is used in conjunction with IOCTL_STORAGE_QUERY_PROPERTY to return temperature data from a storage device or adapter.
helpviewer_keywords: ["*PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR","PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR","PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR structure pointer [Files]","STORAGE_TEMPERATURE_DATA_DESCRIPTOR","STORAGE_TEMPERATURE_DATA_DESCRIPTOR structure [Files]","fs.storage_temperature_data_descriptor","winioctl/PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR","winioctl/STORAGE_TEMPERATURE_DATA_DESCRIPTOR"]
old-location: fs\storage_temperature_data_descriptor.htm
tech.root: fs
ms.assetid: E155B31F-6543-42E3-BCAB-B1B0100D23E4
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR, PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR, PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR structure pointer [Files], STORAGE_TEMPERATURE_DATA_DESCRIPTOR, STORAGE_TEMPERATURE_DATA_DESCRIPTOR structure [Files], fs.storage_temperature_data_descriptor, winioctl/PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR, winioctl/STORAGE_TEMPERATURE_DATA_DESCRIPTOR'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.typenames: STORAGE_TEMPERATURE_DATA_DESCRIPTOR, *PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_TEMPERATURE_DATA_DESCRIPTOR
 - winioctl/_STORAGE_TEMPERATURE_DATA_DESCRIPTOR
 - PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR
 - winioctl/PSTORAGE_TEMPERATURE_DATA_DESCRIPTOR
 - STORAGE_TEMPERATURE_DATA_DESCRIPTOR
 - winioctl/STORAGE_TEMPERATURE_DATA_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - STORAGE_TEMPERATURE_DATA_DESCRIPTOR
---

## -description

This structure is used in conjunction with <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> to return temperature data from a storage device or adapter.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to the structure.

### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this structure.

### -field CriticalTemperature

Indicates the minimum temperature in degrees Celsius that may prevent normal operation. Exceeding this temperature may result in possible data loss, automatic device shutdown, extreme performance throttling, or permanent damage.

### -field WarningTemperature

Indicates the maximum temperature in degrees Celsius at which the device is capable of operating continuously without degrading operation or reliability.

### -field InfoCount

Specifies the number of <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_temperature_info">STORAGE_TEMPERATURE_INFO</a> structures reported in <b>TemperatureInfo</b>. More than one set of temperature data may be returned when there are multiple sensors in the drive.

### -field Reserved0

Reserved for future use.

### -field Reserved1

Reserved for future use.

### -field TemperatureInfo

Device temperature data, of type <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_temperature_info">STORAGE_TEMPERATURE_INFO</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_temperature_threshold">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-storage_property_id">STORAGE_PROPERTY_ID</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_temperature_info">STORAGE_TEMPERATURE_INFO</a>
