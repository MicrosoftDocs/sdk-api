---
UID: NS:webservices._WS_MESSAGE_PROPERTY
title: "_WS_MESSAGE_PROPERTY"
author: windows-sdk-content
description: Specifies a message specific setting.
old-location: wsw\ws_message_property.htm
tech.root: wsw
ms.assetid: 40751692-a8e6-4aa6-8dc9-55308b129a94
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_MESSAGE_PROPERTY, WS_MESSAGE_PROPERTY structure [Web Services for Windows], _WS_MESSAGE_PROPERTY, webservices/WS_MESSAGE_PROPERTY, wsw.ws_message_property
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
 - WS_MESSAGE_PROPERTY
product: Windows
targetos: Windows
req.typenames: WS_MESSAGE_PROPERTY
req.redist: 
---

# _WS_MESSAGE_PROPERTY structure


## -description


Specifies a message specific setting.
            


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_ID</a>.
            


### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size in bytes of the memory pointed to by value.
            

