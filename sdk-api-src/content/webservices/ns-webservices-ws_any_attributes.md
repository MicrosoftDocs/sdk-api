---
UID: NS:webservices._WS_ANY_ATTRIBUTES
title: WS_ANY_ATTRIBUTES (webservices.h)
description: This type is used to store a set of attributes that have not been directly mapped to field of a structure.
helpviewer_keywords: ["WS_ANY_ATTRIBUTES","WS_ANY_ATTRIBUTES structure [Web Services for Windows]","webservices/WS_ANY_ATTRIBUTES","wsw.ws_any_attributes"]
old-location: wsw\ws_any_attributes.htm
tech.root: wsw
ms.assetid: 6c428c99-755f-40ab-bc9e-e1a7a3d70c1d
ms.date: 12/05/2018
ms.keywords: WS_ANY_ATTRIBUTES, WS_ANY_ATTRIBUTES structure [Web Services for Windows], webservices/WS_ANY_ATTRIBUTES, wsw.ws_any_attributes
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_ANY_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ANY_ATTRIBUTES
 - webservices/_WS_ANY_ATTRIBUTES
 - WS_ANY_ATTRIBUTES
 - webservices/WS_ANY_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ANY_ATTRIBUTES
---

# WS_ANY_ATTRIBUTES structure


## -description

This type is used to store a set of attributes
                that have not been directly mapped to field of 
                a structure.

## -struct-fields

### -field attributes

An array of attributes.  This field may
                    be <b>NULL</b> if attributeCount is zero.

### -field attributeCount

The number of attributes in the array.

## -remarks

This structure is typically used to preserve unknown attributes
                when deserializing a structure.
                See <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_ANY_ATTRIBUTES_FIELD_MAPPING</a> and <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_ANY_ATTRIBUTES_TYPE</a> for more
                information.