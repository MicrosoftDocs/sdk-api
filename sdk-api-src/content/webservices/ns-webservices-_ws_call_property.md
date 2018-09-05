---
UID: NS:webservices._WS_CALL_PROPERTY
title: "_WS_CALL_PROPERTY"
author: windows-sdk-content
description: Specifies a proxy property.
old-location: wsw\ws_call_property.htm
old-project: wsw
ms.assetid: 2ab778b2-c6d0-41ea-aa3a-a6c16c87a9e9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_CALL_PROPERTY, WS_CALL_PROPERTY structure [Web Services for Windows], _WS_CALL_PROPERTY, webservices/WS_CALL_PROPERTY, wsw.ws_call_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WS_CALL_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CALL_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_CALL_PROPERTY structure


## -description


Specifies a proxy property.
            


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/d61b6763-9770-4f1d-b16f-c63fc09e8af5">WS_CALL_PROPERTY_ID</a>.
            


### -field value

Pointer to a buffer for the value of the property.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size of buffer in bytes.
            

