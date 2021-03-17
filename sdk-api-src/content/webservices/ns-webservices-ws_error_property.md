---
UID: NS:webservices._WS_ERROR_PROPERTY
title: WS_ERROR_PROPERTY (webservices.h)
description: Specifies an error specific setting.
helpviewer_keywords: ["WS_ERROR_PROPERTY","WS_ERROR_PROPERTY structure [Web Services for Windows]","webservices/WS_ERROR_PROPERTY","wsw.ws_error_property"]
old-location: wsw\ws_error_property.htm
tech.root: wsw
ms.assetid: 463b634f-bb15-494d-8061-c4fa0b97b990
ms.date: 12/05/2018
ms.keywords: WS_ERROR_PROPERTY, WS_ERROR_PROPERTY structure [Web Services for Windows], webservices/WS_ERROR_PROPERTY, wsw.ws_error_property
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
req.typenames: WS_ERROR_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ERROR_PROPERTY
 - webservices/_WS_ERROR_PROPERTY
 - WS_ERROR_PROPERTY
 - webservices/WS_ERROR_PROPERTY
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
 - WS_ERROR_PROPERTY
---

# WS_ERROR_PROPERTY structure


## -description

Specifies an error specific setting.

## -struct-fields

### -field id

Identifies the <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.

### -field valueSize

The size, in bytes, of the memory pointed to by value.