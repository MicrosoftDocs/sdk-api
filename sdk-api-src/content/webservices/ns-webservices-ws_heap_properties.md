---
UID: NS:webservices._WS_HEAP_PROPERTIES
title: WS_HEAP_PROPERTIES (webservices.h)
description: A structure that is used to specify a set of WS_HEAP_PROPERTYs.
helpviewer_keywords: ["WS_HEAP_PROPERTIES","WS_HEAP_PROPERTIES structure [Web Services for Windows]","webservices/WS_HEAP_PROPERTIES","wsw.ws_heap_properties"]
old-location: wsw\ws_heap_properties.htm
tech.root: wsw
ms.assetid: d367bb85-514d-4acc-b67f-f7381a9a6404
ms.date: 12/05/2018
ms.keywords: WS_HEAP_PROPERTIES, WS_HEAP_PROPERTIES structure [Web Services for Windows], webservices/WS_HEAP_PROPERTIES, wsw.ws_heap_properties
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
req.typenames: WS_HEAP_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HEAP_PROPERTIES
 - webservices/_WS_HEAP_PROPERTIES
 - WS_HEAP_PROPERTIES
 - webservices/WS_HEAP_PROPERTIES
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
 - WS_HEAP_PROPERTIES
---

# WS_HEAP_PROPERTIES structure


## -description

A structure that is used to specify a set of <a href="/windows/desktop/api/webservices/ns-webservices-ws_heap_property">WS_HEAP_PROPERTY</a>s.

## -struct-fields

### -field properties

An array of properties.  The number of elements in the array is specified
                    using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                    is 0.

### -field propertyCount

The number of elements in the properties array.