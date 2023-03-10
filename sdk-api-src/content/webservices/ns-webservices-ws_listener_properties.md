---
UID: NS:webservices._WS_LISTENER_PROPERTIES
title: WS_LISTENER_PROPERTIES (webservices.h)
description: Specifies a set of WS_LISTENER_PROPERTY structures.
helpviewer_keywords: ["WS_LISTENER_PROPERTIES","WS_LISTENER_PROPERTIES structure [Web Services for Windows]","webservices/WS_LISTENER_PROPERTIES","wsw.ws_listener_properties"]
old-location: wsw\ws_listener_properties.htm
tech.root: wsw
ms.assetid: 19619c20-d287-42d8-9326-15c810619f22
ms.date: 12/05/2018
ms.keywords: WS_LISTENER_PROPERTIES, WS_LISTENER_PROPERTIES structure [Web Services for Windows], webservices/WS_LISTENER_PROPERTIES, wsw.ws_listener_properties
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
req.typenames: WS_LISTENER_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_LISTENER_PROPERTIES
 - webservices/_WS_LISTENER_PROPERTIES
 - WS_LISTENER_PROPERTIES
 - webservices/WS_LISTENER_PROPERTIES
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
 - WS_LISTENER_PROPERTIES
---

# WS_LISTENER_PROPERTIES structure


## -description

Specifies a set of <a href="/windows/desktop/api/webservices/ns-webservices-ws_listener_property">WS_LISTENER_PROPERTY</a> structures.

## -struct-fields

### -field properties

An array of properties.  The number of elements in the array is specified
                    using the <b>propertyCount</b> member.  This field may be <b>NULL</b> if the propertyCount
                    is 0.

### -field propertyCount

The number of elements in the properties array.