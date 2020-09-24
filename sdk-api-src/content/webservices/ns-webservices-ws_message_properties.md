---
UID: NS:webservices._WS_MESSAGE_PROPERTIES
title: WS_MESSAGE_PROPERTIES (webservices.h)
description: Specifies a set of WS_MESSAGE_PROPERTY structures.
helpviewer_keywords: ["WS_MESSAGE_PROPERTIES","WS_MESSAGE_PROPERTIES structure [Web Services for Windows]","webservices/WS_MESSAGE_PROPERTIES","wsw.ws_message_properties"]
old-location: wsw\ws_message_properties.htm
tech.root: wsw
ms.assetid: 74ad74fd-457a-4408-8032-15d365f98b14
ms.date: 12/05/2018
ms.keywords: WS_MESSAGE_PROPERTIES, WS_MESSAGE_PROPERTIES structure [Web Services for Windows], webservices/WS_MESSAGE_PROPERTIES, wsw.ws_message_properties
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_MESSAGE_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_MESSAGE_PROPERTIES
 - webservices/_WS_MESSAGE_PROPERTIES
 - WS_MESSAGE_PROPERTIES
 - webservices/WS_MESSAGE_PROPERTIES
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
 - WS_MESSAGE_PROPERTIES
---

# WS_MESSAGE_PROPERTIES structure


## -description

Specifies a set of <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_property">WS_MESSAGE_PROPERTY</a> structures.

## -struct-fields

### -field properties

An array of properties.  The number of elements in the array is specified
                    using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                    is 0.

### -field propertyCount

The number of elements in the properties array.