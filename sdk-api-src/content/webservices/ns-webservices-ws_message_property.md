---
UID: NS:webservices._WS_MESSAGE_PROPERTY
title: WS_MESSAGE_PROPERTY (webservices.h)
description: Specifies a message specific setting.
helpviewer_keywords: ["WS_MESSAGE_PROPERTY","WS_MESSAGE_PROPERTY structure [Web Services for Windows]","webservices/WS_MESSAGE_PROPERTY","wsw.ws_message_property"]
old-location: wsw\ws_message_property.htm
tech.root: wsw
ms.assetid: 40751692-a8e6-4aa6-8dc9-55308b129a94
ms.date: 12/05/2018
ms.keywords: WS_MESSAGE_PROPERTY, WS_MESSAGE_PROPERTY structure [Web Services for Windows], webservices/WS_MESSAGE_PROPERTY, wsw.ws_message_property
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
req.typenames: WS_MESSAGE_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_MESSAGE_PROPERTY
 - webservices/_WS_MESSAGE_PROPERTY
 - WS_MESSAGE_PROPERTY
 - webservices/WS_MESSAGE_PROPERTY
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
 - WS_MESSAGE_PROPERTY
---

# WS_MESSAGE_PROPERTY structure


## -description

Specifies a message specific setting.

## -struct-fields

### -field id

Identifies the <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.

### -field valueSize

The size in bytes of the memory pointed to by value.