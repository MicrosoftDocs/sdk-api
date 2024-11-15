---
UID: NS:wsdtypes._WSD_THIS_DEVICE_METADATA
title: WSD_THIS_DEVICE_METADATA (wsdtypes.h)
description: Specifies metadata that is unique to a specific device.
helpviewer_keywords: ["WSD_THIS_DEVICE_METADATA","WSD_THIS_DEVICE_METADATA structure","ncd.wsd_this_device_metadata_struct","wsdtypes/WSD_THIS_DEVICE_METADATA"]
old-location: ncd\wsd_this_device_metadata_struct.htm
tech.root: ncd
ms.assetid: 7b9d063f-f0d5-4333-a5d8-e9a6d2d9af88
ms.date: 12/05/2018
ms.keywords: WSD_THIS_DEVICE_METADATA, WSD_THIS_DEVICE_METADATA structure, ncd.wsd_this_device_metadata_struct, wsdtypes/WSD_THIS_DEVICE_METADATA
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WSD_THIS_DEVICE_METADATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_THIS_DEVICE_METADATA
 - wsdtypes/_WSD_THIS_DEVICE_METADATA
 - WSD_THIS_DEVICE_METADATA
 - wsdtypes/WSD_THIS_DEVICE_METADATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_THIS_DEVICE_METADATA
---

# WSD_THIS_DEVICE_METADATA structure


## -description

Specifies metadata that is unique to a specific device.

## -struct-fields

### -field FriendlyName

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_localized_string_list">WSD_LOCALIZED_STRING_LIST</a> structure that contains the list of localized friendly names for the device. It should be set to fewer than 256 characters.

### -field FirmwareVersion

The firmware version of the device. It should be set to fewer than 256 characters.

### -field SerialNumber

The serial number of the device. It should be set to fewer than 256 characters.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that provides an extensible space for devices to add custom metadata to the device specific section. For example, you can use this to add a user-defined name for the device.

## -remarks

ThisDevice metadata follows this form:

``` syntax
<wsd:ThisDevice>
    <wsd:FriendlyName>
        A. Datum WebWeigh Scale
    </wsd:FriendlyName>
    <wsd:FirmwareVersion>
        2.53c
    </wsd:FirmwareVersion>
    <wsd:SerialNumber>
        923450982349058
    </wsd:SerialNumber>
 </wsd:ThisDevice>
```

