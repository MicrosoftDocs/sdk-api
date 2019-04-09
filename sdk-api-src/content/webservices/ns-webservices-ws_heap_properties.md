---
UID: NS:webservices._WS_HEAP_PROPERTIES
title: WS_HEAP_PROPERTIES (webservices.h)
author: windows-sdk-content
description: A structure that is used to specify a set of WS_HEAP_PROPERTYs.
old-location: wsw\ws_heap_properties.htm
tech.root: wsw
ms.assetid: d367bb85-514d-4acc-b67f-f7381a9a6404
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_HEAP_PROPERTIES, WS_HEAP_PROPERTIES structure [Web Services for Windows], webservices/WS_HEAP_PROPERTIES, wsw.ws_heap_properties
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_HEAP_PROPERTIES
product: Windows
targetos: Windows
req.typenames: WS_HEAP_PROPERTIES
req.redist: 
---

# WS_HEAP_PROPERTIES structure


## -description


A structure that is used to specify a set of <a href="https://msdn.microsoft.com/e55122e4-fc18-4e1a-b34e-c661b555a062">WS_HEAP_PROPERTY</a>s.
            


## -struct-fields




### -field properties

An array of properties.  The number of elements in the array is specified
                    using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                    is 0.
                


### -field propertyCount

The number of elements in the properties array.
                

