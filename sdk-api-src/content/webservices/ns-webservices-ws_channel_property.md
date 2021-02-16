---
UID: NS:webservices._WS_CHANNEL_PROPERTY
title: WS_CHANNEL_PROPERTY (webservices.h)
description: Specifies a channel specific setting.
helpviewer_keywords: ["WS_CHANNEL_PROPERTY","WS_CHANNEL_PROPERTY structure [Web Services for Windows]","webservices/WS_CHANNEL_PROPERTY","wsw.ws_channel_property"]
old-location: wsw\ws_channel_property.htm
tech.root: wsw
ms.assetid: 0298e8ae-67ad-4881-885f-2ed713316e76
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_PROPERTY, WS_CHANNEL_PROPERTY structure [Web Services for Windows], webservices/WS_CHANNEL_PROPERTY, wsw.ws_channel_property
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
req.typenames: WS_CHANNEL_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CHANNEL_PROPERTY
 - webservices/_WS_CHANNEL_PROPERTY
 - WS_CHANNEL_PROPERTY
 - webservices/WS_CHANNEL_PROPERTY
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
 - WS_CHANNEL_PROPERTY
---

# WS_CHANNEL_PROPERTY structure


## -description

Specifies a channel specific setting.

## -struct-fields

### -field id

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -field valueSize

The size in bytes of the memory pointed to by the <b>value</b> member.