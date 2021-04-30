---
UID: NS:webservices._WS_METADATA_PROPERTY
title: WS_METADATA_PROPERTY (webservices.h)
description: Specifies a metadata object setting.
helpviewer_keywords: ["WS_METADATA_PROPERTY","WS_METADATA_PROPERTY structure [Web Services for Windows]","webservices/WS_METADATA_PROPERTY","wsw.ws_metadata_property"]
old-location: wsw\ws_metadata_property.htm
tech.root: wsw
ms.assetid: 72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4
ms.date: 12/05/2018
ms.keywords: WS_METADATA_PROPERTY, WS_METADATA_PROPERTY structure [Web Services for Windows], webservices/WS_METADATA_PROPERTY, wsw.ws_metadata_property
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
req.typenames: WS_METADATA_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_METADATA_PROPERTY
 - webservices/_WS_METADATA_PROPERTY
 - WS_METADATA_PROPERTY
 - webservices/WS_METADATA_PROPERTY
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
 - WS_METADATA_PROPERTY
---

# WS_METADATA_PROPERTY structure


## -description

Specifies a metadata object setting.

## -struct-fields

### -field id

Identifies the <a href="/windows/desktop/api/webservices/ne-webservices-ws_metadata_property_id">WS_METADATA_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -field valueSize

The size in bytes of the memory pointed to by value.