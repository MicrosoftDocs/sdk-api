---
UID: NS:webservices._WS_SECURITY_BINDING_PROPERTY
title: WS_SECURITY_BINDING_PROPERTY (webservices.h)
author: windows-sdk-content
description: Specifies a security binding specific setting.
old-location: wsw\ws_security_binding_property.htm
tech.root: wsw
ms.assetid: f2790fd7-6f51-45a5-b2b6-e5aaaaca9660
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_BINDING_PROPERTY, WS_SECURITY_BINDING_PROPERTY structure [Web Services for Windows], webservices/WS_SECURITY_BINDING_PROPERTY, wsw.ws_security_binding_property
ms.topic: struct
f1_keywords: 
 - "webservices/WS_SECURITY_BINDING_PROPERTY"
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
 - WS_SECURITY_BINDING_PROPERTY
targetos: Windows
req.typenames: WS_SECURITY_BINDING_PROPERTY
req.redist: 
ms.custom: 19H1
---

# WS_SECURITY_BINDING_PROPERTY structure


## -description


Specifies a security binding specific setting.
            


## -struct-fields




### -field id

Identifies the <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_ID</a>.
            


### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size, in bytes, of the memory pointed to by value.
            

