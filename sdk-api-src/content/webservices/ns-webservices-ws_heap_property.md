---
UID: NS:webservices._WS_HEAP_PROPERTY
title: WS_HEAP_PROPERTY (webservices.h)
description: Specifies a heap specific setting.
helpviewer_keywords: ["WS_HEAP_PROPERTY","WS_HEAP_PROPERTY structure [Web Services for Windows]","webservices/WS_HEAP_PROPERTY","wsw.ws_heap_property"]
old-location: wsw\ws_heap_property.htm
tech.root: wsw
ms.assetid: e55122e4-fc18-4e1a-b34e-c661b555a062
ms.date: 12/05/2018
ms.keywords: WS_HEAP_PROPERTY, WS_HEAP_PROPERTY structure [Web Services for Windows], webservices/WS_HEAP_PROPERTY, wsw.ws_heap_property
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
req.typenames: WS_HEAP_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HEAP_PROPERTY
 - webservices/_WS_HEAP_PROPERTY
 - WS_HEAP_PROPERTY
 - webservices/WS_HEAP_PROPERTY
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
 - WS_HEAP_PROPERTY
---

# WS_HEAP_PROPERTY structure


## -description

Specifies a heap specific setting.

## -struct-fields

### -field id

Identifies the <a href="/windows/desktop/api/webservices/ne-webservices-ws_heap_property_id">WS_HEAP_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.

### -field valueSize

The size in bytes of the memory pointed to by value.