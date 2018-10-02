---
UID: NS:webservices._WS_HEAP_PROPERTY
title: "_WS_HEAP_PROPERTY"
author: windows-sdk-content
description: Specifies a heap specific setting.
old-location: wsw\ws_heap_property.htm
tech.root: wsw
ms.assetid: e55122e4-fc18-4e1a-b34e-c661b555a062
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_HEAP_PROPERTY, WS_HEAP_PROPERTY structure [Web Services for Windows], _WS_HEAP_PROPERTY, webservices/WS_HEAP_PROPERTY, wsw.ws_heap_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_HEAP_PROPERTY
product: Windows
targetos: Windows
req.typenames: WS_HEAP_PROPERTY
req.redist: 
---

# _WS_HEAP_PROPERTY structure


## -description


Specifies a heap specific setting.
            


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/c047a3b9-27a1-464c-b9f9-0b0c6cf8eb97">WS_HEAP_PROPERTY_ID</a>.
            


### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size in bytes of the memory pointed to by value.
            

