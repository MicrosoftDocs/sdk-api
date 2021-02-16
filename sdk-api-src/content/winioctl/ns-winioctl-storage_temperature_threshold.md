---
UID: NS:winioctl._STORAGE_TEMPERATURE_THRESHOLD
title: STORAGE_TEMPERATURE_THRESHOLD
description: This structure is used to set the over or under temperature threshold of a storage device (via IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD).
helpviewer_keywords: ["*PSTORAGE_TEMPERATURE_THRESHOLD","PSTORAGE_TEMPERATURE_THRESHOLD","PSTORAGE_TEMPERATURE_THRESHOLD structure pointer [Files]","STORAGE_TEMPERATURE_THRESHOLD","STORAGE_TEMPERATURE_THRESHOLD structure [Files]","fs.storage_temperature_threshold","winioctl/PSTORAGE_TEMPERATURE_THRESHOLD","winioctl/STORAGE_TEMPERATURE_THRESHOLD"]
old-location: fs\storage_temperature_threshold.htm
tech.root: fs
ms.assetid: 02E01EAE-FF0F-4013-A237-651B1428DF52
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_TEMPERATURE_THRESHOLD, PSTORAGE_TEMPERATURE_THRESHOLD, PSTORAGE_TEMPERATURE_THRESHOLD structure pointer [Files], STORAGE_TEMPERATURE_THRESHOLD, STORAGE_TEMPERATURE_THRESHOLD structure [Files], fs.storage_temperature_threshold, winioctl/PSTORAGE_TEMPERATURE_THRESHOLD, winioctl/STORAGE_TEMPERATURE_THRESHOLD'
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
req.typenames: STORAGE_TEMPERATURE_THRESHOLD, *PSTORAGE_TEMPERATURE_THRESHOLD
req.redist: 
f1_keywords:
 - _STORAGE_TEMPERATURE_THRESHOLD
 - winioctl/_STORAGE_TEMPERATURE_THRESHOLD
 - PSTORAGE_TEMPERATURE_THRESHOLD
 - winioctl/PSTORAGE_TEMPERATURE_THRESHOLD
 - STORAGE_TEMPERATURE_THRESHOLD
 - winioctl/STORAGE_TEMPERATURE_THRESHOLD
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
 - STORAGE_TEMPERATURE_THRESHOLD
---

# STORAGE_TEMPERATURE_THRESHOLD structure


## -description

This structure is used to set the over or under temperature threshold of a storage device (via <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_temperature_threshold">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>).

## -struct-fields

### -field Version

The version of the structure.

### -field Size

The size of this structure. This should be set to sizeof(<b>STORAGE_TEMPERATURE_THRESHOLD</b>).

### -field Flags

Flags set for this request. The following are valid flags.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST</b></td>
<td>This flag indicates the request to target an adapter instead of device.</td>
</tr>
</table>

### -field Index

Identifies the instance of temperature information. Starts from 0. Index 0 may indicate a composite value.

### -field Threshold

A signed value that indicates the temperature of the threshold, in degrees Celsius.

### -field OverThreshold

Indicates if the <i>Threshold</i> specifies the over or under temperature threshold. If <b>true</b>, set the <b>OverThreshold</b> temperature value of the device; otherwise, set the <b>UnderThreshold</b> temperature value.

### -field Reserved

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_set_temperature_threshold">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-storage_property_id">STORAGE_PROPERTY_ID</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_temperature_info">STORAGE_TEMPERATURE_INFO</a>