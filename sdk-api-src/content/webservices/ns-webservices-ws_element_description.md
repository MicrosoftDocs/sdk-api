---
UID: NS:webservices._WS_ELEMENT_DESCRIPTION
title: WS_ELEMENT_DESCRIPTION (webservices.h)
description: Represents a mapping between a C data type and an XML element.
helpviewer_keywords: ["WS_ELEMENT_DESCRIPTION","WS_ELEMENT_DESCRIPTION structure [Web Services for Windows]","webservices/WS_ELEMENT_DESCRIPTION","wsw.ws_element_description"]
old-location: wsw\ws_element_description.htm
tech.root: wsw
ms.assetid: 17035b64-9b2c-40d3-bdce-45e9b132e9f1
ms.date: 12/05/2018
ms.keywords: WS_ELEMENT_DESCRIPTION, WS_ELEMENT_DESCRIPTION structure [Web Services for Windows], webservices/WS_ELEMENT_DESCRIPTION, wsw.ws_element_description
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_ELEMENT_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ELEMENT_DESCRIPTION
 - webservices/_WS_ELEMENT_DESCRIPTION
 - WS_ELEMENT_DESCRIPTION
 - webservices/WS_ELEMENT_DESCRIPTION
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
 - WS_ELEMENT_DESCRIPTION
---

# WS_ELEMENT_DESCRIPTION structure


## -description

Represents a mapping between a C data type and an XML element.

## -struct-fields

### -field elementLocalName

The local name of the XML element.

### -field elementNs

The namespace of the XML element.

### -field type

The type that corresponds to this XML element.
                

Not all types support being read and written as an element.  If the
                    documentation for the <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a> indicates it supports
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_ELEMENT_TYPE_MAPPING</a>, then it can be used with this structure.

### -field typeDescription

Additional information about the type.  Each type has a different description
                    structure.  This may be <b>NULL</b>, depending on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>.