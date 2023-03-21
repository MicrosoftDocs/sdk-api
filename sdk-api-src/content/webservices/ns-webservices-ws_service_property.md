---
UID: NS:webservices._WS_SERVICE_PROPERTY
title: WS_SERVICE_PROPERTY (webservices.h)
description: Specifies a service specific setting. (WS_SERVICE_PROPERTY)
helpviewer_keywords: ["WS_SERVICE_PROPERTY","WS_SERVICE_PROPERTY structure [Web Services for Windows]","webservices/WS_SERVICE_PROPERTY","wsw.ws_service_property"]
old-location: wsw\ws_service_property.htm
tech.root: wsw
ms.assetid: d25cab25-2227-4afe-ae45-93a229d7f78b
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_PROPERTY, WS_SERVICE_PROPERTY structure [Web Services for Windows], webservices/WS_SERVICE_PROPERTY, wsw.ws_service_property
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
req.typenames: WS_SERVICE_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SERVICE_PROPERTY
 - webservices/_WS_SERVICE_PROPERTY
 - WS_SERVICE_PROPERTY
 - webservices/WS_SERVICE_PROPERTY
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
 - WS_SERVICE_PROPERTY
---

# WS_SERVICE_PROPERTY structure


## -description

Specifies a service specific setting.

## -struct-fields

### -field id

Identifies the <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_property_id">WS_SERVICE_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.

### -field valueSize

The size, in bytes, of the memory pointed to by value.
