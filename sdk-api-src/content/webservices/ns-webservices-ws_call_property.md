---
UID: NS:webservices._WS_CALL_PROPERTY
title: WS_CALL_PROPERTY (webservices.h)
description: Specifies a proxy property. (WS_CALL_PROPERTY)
helpviewer_keywords: ["WS_CALL_PROPERTY","WS_CALL_PROPERTY structure [Web Services for Windows]","webservices/WS_CALL_PROPERTY","wsw.ws_call_property"]
old-location: wsw\ws_call_property.htm
tech.root: wsw
ms.assetid: 2ab778b2-c6d0-41ea-aa3a-a6c16c87a9e9
ms.date: 12/05/2018
ms.keywords: WS_CALL_PROPERTY, WS_CALL_PROPERTY structure [Web Services for Windows], webservices/WS_CALL_PROPERTY, wsw.ws_call_property
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
req.typenames: WS_CALL_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CALL_PROPERTY
 - webservices/_WS_CALL_PROPERTY
 - WS_CALL_PROPERTY
 - webservices/WS_CALL_PROPERTY
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
 - WS_CALL_PROPERTY
---

# WS_CALL_PROPERTY structure


## -description

Specifies a proxy property.

## -struct-fields

### -field id

Identifies the <a href="/windows/desktop/api/webservices/ne-webservices-ws_call_property_id">WS_CALL_PROPERTY_ID</a>.

### -field value

Pointer to a buffer for the value of the property.
                The pointer must have an alignment compatible with the type
                of the property.

### -field valueSize

The size of buffer in bytes.
