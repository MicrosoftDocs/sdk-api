---
UID: NS:webservices._WS_XML_SECURITY_TOKEN_PROPERTY
title: WS_XML_SECURITY_TOKEN_PROPERTY (webservices.h)
description: Specifies a property for an XML security token.
helpviewer_keywords: ["WS_XML_SECURITY_TOKEN_PROPERTY","WS_XML_SECURITY_TOKEN_PROPERTY structure [Web Services for Windows]","webservices/WS_XML_SECURITY_TOKEN_PROPERTY","wsw.ws_xml_security_token_property"]
old-location: wsw\ws_xml_security_token_property.htm
tech.root: wsw
ms.assetid: dd235e33-39f7-459d-8b7f-76d5c3f96770
ms.date: 12/05/2018
ms.keywords: WS_XML_SECURITY_TOKEN_PROPERTY, WS_XML_SECURITY_TOKEN_PROPERTY structure [Web Services for Windows], webservices/WS_XML_SECURITY_TOKEN_PROPERTY, wsw.ws_xml_security_token_property
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
req.typenames: WS_XML_SECURITY_TOKEN_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_SECURITY_TOKEN_PROPERTY
 - webservices/_WS_XML_SECURITY_TOKEN_PROPERTY
 - WS_XML_SECURITY_TOKEN_PROPERTY
 - webservices/WS_XML_SECURITY_TOKEN_PROPERTY
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
 - WS_XML_SECURITY_TOKEN_PROPERTY
---

# WS_XML_SECURITY_TOKEN_PROPERTY structure


## -description

Specifies a property for an XML security token.

## -struct-fields

### -field id

Identifies the <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_security_token_property_id">WS_XML_SECURITY_TOKEN_PROPERTY_ID</a>.

### -field value

A pointer to the value.
                The pointer must have an alignment compatible with the type
                of the property.

### -field valueSize

The size in bytes of the memory pointed to by value.