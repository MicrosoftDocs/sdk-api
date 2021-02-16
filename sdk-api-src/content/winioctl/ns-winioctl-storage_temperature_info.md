---
UID: NS:winioctl._STORAGE_TEMPERATURE_INFO
title: STORAGE_TEMPERATURE_INFO
description: Describes device temperature data. Returned as part of STORAGE_TEMPERATURE_DATA_DESCRIPTOR when querying for temperature data with an IOCTL_STORAGE_QUERY_PROPERTY request.
helpviewer_keywords: ["*PSTORAGE_TEMPERATURE_INFO","PSTORAGE_TEMPERATURE_INFO","PSTORAGE_TEMPERATURE_INFO structure pointer [Files]","STORAGE_TEMPERATURE_INFO","STORAGE_TEMPERATURE_INFO structure [Files]","fs.storage_temperature_info","winioctl/PSTORAGE_TEMPERATURE_INFO","winioctl/STORAGE_TEMPERATURE_INFO"]
old-location: fs\storage_temperature_info.htm
tech.root: fs
ms.assetid: 236B4AC7-AF5E-4556-9FFD-D64C450E6492
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_TEMPERATURE_INFO, PSTORAGE_TEMPERATURE_INFO, PSTORAGE_TEMPERATURE_INFO structure pointer [Files], STORAGE_TEMPERATURE_INFO, STORAGE_TEMPERATURE_INFO structure [Files], fs.storage_temperature_info, winioctl/PSTORAGE_TEMPERATURE_INFO, winioctl/STORAGE_TEMPERATURE_INFO'
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
req.typenames: STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO
req.redist: 
f1_keywords:
 - _STORAGE_TEMPERATURE_INFO
 - winioctl/_STORAGE_TEMPERATURE_INFO
 - PSTORAGE_TEMPERATURE_INFO
 - winioctl/PSTORAGE_TEMPERATURE_INFO
 - STORAGE_TEMPERATURE_INFO
 - winioctl/STORAGE_TEMPERATURE_INFO
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
 - STORAGE_TEMPERATURE_INFO
---

# STORAGE_TEMPERATURE_INFO structure


## -description

Describes  device temperature data. Returned as part of <a href="/windows/win32/api/winioctl/ns-winioctl-storage_temperature_data_descriptor">STORAGE_TEMPERATURE_DATA_DESCRIPTOR</a> when querying for temperature data with an <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request.

## -struct-fields

### -field Index

Identifies the instance of temperature information. Starts from 0. Index 0 may indicate a composite value.

### -field Temperature

A signed value that indicates the current temperature, in degrees Celsius.

### -field OverThreshold

A signed value that specifies the maximum temperature within the desired threshold, in degrees Celsius.

### -field UnderThreshold

A signed value that specifies the minimum temperature within the desired threshold, in degrees Celsius.

### -field OverThresholdChangable

Indicates if <i>OverThreshold</i> can be changed by using <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_temperature_threshold">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>.

### -field UnderThresholdChangable

Indicates if <i>UnderThreshold</i> can be changed by using <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_temperature_threshold">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>.

### -field EventGenerated

Indicates if a notification will be generated when the current temperature crosses a threshold.

### -field Reserved0

Reserved for future use.

### -field Reserved1

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_temperature_threshold">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-storage_property_id">STORAGE_PROPERTY_ID</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>