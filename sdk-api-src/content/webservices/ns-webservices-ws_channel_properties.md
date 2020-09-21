---
UID: NS:webservices._WS_CHANNEL_PROPERTIES
title: WS_CHANNEL_PROPERTIES (webservices.h)
description: Specifies a set of WS_CHANNEL_PROPERTY structures.
helpviewer_keywords: ["WS_CHANNEL_PROPERTIES","WS_CHANNEL_PROPERTIES structure [Web Services for Windows]","webservices/WS_CHANNEL_PROPERTIES","wsw.ws_channel_properties"]
old-location: wsw\ws_channel_properties.htm
tech.root: wsw
ms.assetid: a28eddde-2b95-4655-962b-1d04b7a2c5fe
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_PROPERTIES, WS_CHANNEL_PROPERTIES structure [Web Services for Windows], webservices/WS_CHANNEL_PROPERTIES, wsw.ws_channel_properties
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
req.typenames: WS_CHANNEL_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CHANNEL_PROPERTIES
 - webservices/_WS_CHANNEL_PROPERTIES
 - WS_CHANNEL_PROPERTIES
 - webservices/WS_CHANNEL_PROPERTIES
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
 - WS_CHANNEL_PROPERTIES
---

# WS_CHANNEL_PROPERTIES structure


## -description

Specifies a set of <a href="/windows/desktop/api/webservices/ns-webservices-ws_channel_property">WS_CHANNEL_PROPERTY</a> structures.

## -struct-fields

### -field properties

An array of properties.  The number of elements in the array is specified
                    using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                    is 0.

### -field propertyCount

The number of elements in the properties array.