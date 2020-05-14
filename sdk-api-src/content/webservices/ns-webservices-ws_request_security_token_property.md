---
UID: NS:webservices._WS_REQUEST_SECURITY_TOKEN_PROPERTY
title: WS_REQUEST_SECURITY_TOKEN_PROPERTY (webservices.h)
description: Specifies a property for requesting a security token from an issuer.helpviewer_keywords: ["WS_REQUEST_SECURITY_TOKEN_PROPERTY","WS_REQUEST_SECURITY_TOKEN_PROPERTY structure [Web Services for Windows]","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY","wsw.ws_request_security_token_property"]
old-location: wsw\ws_request_security_token_property.htm
tech.root: wsw
ms.assetid: ebf6d821-f540-4c89-a2f8-c795a3688e0d
ms.date: 12/05/2018
ms.keywords: WS_REQUEST_SECURITY_TOKEN_PROPERTY, WS_REQUEST_SECURITY_TOKEN_PROPERTY structure [Web Services for Windows], webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY, wsw.ws_request_security_token_property
f1_keywords:
- webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WebServices.h
api_name:
- WS_REQUEST_SECURITY_TOKEN_PROPERTY
targetos: Windows
req.typenames: WS_REQUEST_SECURITY_TOKEN_PROPERTY
req.redist: 
ms.custom: 19H1
---

# WS_REQUEST_SECURITY_TOKEN_PROPERTY structure


## -description


Specifies a property for requesting a security token from an issuer.
            


## -struct-fields




### -field id

Identifies the <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_request_security_token_property_id">WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID</a>.
            


### -field value

A pointer to the value.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size in bytes of the memory pointed to by value.
            

