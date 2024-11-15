---
UID: NS:wsdtypes._WSD_THIS_MODEL_METADATA
title: WSD_THIS_MODEL_METADATA (wsdtypes.h)
description: Provides model-specific information relating to the device.
helpviewer_keywords: ["WSD_THIS_MODEL_METADATA","WSD_THIS_MODEL_METADATA structure","ncd.wsd_this_model_metadata_struct","wsdtypes/WSD_THIS_MODEL_METADATA"]
old-location: ncd\wsd_this_model_metadata_struct.htm
tech.root: ncd
ms.assetid: 614daaeb-76ac-4dec-93fe-f413164d5330
ms.date: 12/05/2018
ms.keywords: WSD_THIS_MODEL_METADATA, WSD_THIS_MODEL_METADATA structure, ncd.wsd_this_model_metadata_struct, wsdtypes/WSD_THIS_MODEL_METADATA
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
req.typenames: WSD_THIS_MODEL_METADATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_THIS_MODEL_METADATA
 - wsdtypes/_WSD_THIS_MODEL_METADATA
 - WSD_THIS_MODEL_METADATA
 - wsdtypes/WSD_THIS_MODEL_METADATA
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
 - WSD_THIS_MODEL_METADATA
---

# WSD_THIS_MODEL_METADATA structure


## -description

Provides model-specific information relating to the device.

## -struct-fields

### -field Manufacturer

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_localized_string_list">WSD_LOCALIZED_STRING_LIST</a> structure that contains the manufacturer name. The name should be set to fewer than 2048 characters.

### -field ManufacturerUrl

The URL to a Web site for the device manufacturer. The URL should have fewer than 2048 characters.

### -field ModelName

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_localized_string_list">WSD_LOCALIZED_STRING_LIST</a> structure that specifies model names. This is a list of localized friendly names that should be set to fewer than 256 characters.

### -field ModelNumber

The model number. This should be set to fewer than 256 characters.

### -field ModelUrl

The URL to a Web site for this device model. The URL should have fewer than 2048 characters.

### -field PresentationUrl

An HTML page for this device. This can be relative to a base URL set by XML Base. The URL should have fewer than 2048 characters.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -remarks

<b>WSD_THIS_MODEL_METADATA</b> specifies manufacturer metadata that is common to all instances of a specific model.

Model metadata follows this form:

``` syntax
<wsd:ThisModel>
    <wsd:Manufacturer>
        A. Datum Corporation
    </wsd:Manufacturer>
    <wsd:ManufacturerURL>
        http://www.adatum.com
    </wsd:ManufacturerURL>
    <wsd:ModelName>
        WebWeigh
    </wsd:ModelName>
    <wsd:ModelNumber>
        9-23492-83049
    </wsd:ModelNumber>
    <wsd:ModelURL>
        http://www.adatum.com/WebWeighOwner.html
    </wsd:ModelURL>
    <wsd:PresentationURL>
        presentation/menu.html
    </wsd:PresentationURL>
</wsd:ThisModel>
```

