---
UID: NS:webservices._WS_XML_BUFFER_PROPERTY
title: WS_XML_BUFFER_PROPERTY (webservices.h)
description: Specifies an XML buffer specific setting.
helpviewer_keywords: ["WS_XML_BUFFER_PROPERTY","WS_XML_BUFFER_PROPERTY structure [Web Services for Windows]","webservices/WS_XML_BUFFER_PROPERTY","wsw.ws_xml_buffer_property"]
old-location: wsw\ws_xml_buffer_property.htm
tech.root: wsw
ms.assetid: bec8d297-7f5a-4b8f-a333-9b535358c470
ms.date: 12/05/2018
ms.keywords: WS_XML_BUFFER_PROPERTY, WS_XML_BUFFER_PROPERTY structure [Web Services for Windows], webservices/WS_XML_BUFFER_PROPERTY, wsw.ws_xml_buffer_property
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
req.typenames: WS_XML_BUFFER_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_BUFFER_PROPERTY
 - webservices/_WS_XML_BUFFER_PROPERTY
 - WS_XML_BUFFER_PROPERTY
 - webservices/WS_XML_BUFFER_PROPERTY
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
 - WS_XML_BUFFER_PROPERTY
---

# WS_XML_BUFFER_PROPERTY structure


## -description

Specifies an XML buffer–specific setting.

## -struct-fields

### -field id

Identifies the <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id">WS_XML_BUFFER_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
            The pointer must have an alignment compatible with the type
            of the property.

### -field valueSize

The size in bytes of the memory pointed to by value.

