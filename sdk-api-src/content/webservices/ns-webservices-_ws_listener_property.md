---
UID: NS:webservices._WS_LISTENER_PROPERTY
title: "_WS_LISTENER_PROPERTY"
author: windows-sdk-content
description: Specifies a listener specific setting.
old-location: wsw\ws_listener_property.htm
old-project: wsw
ms.assetid: 52e4a5d3-e584-40d1-b71f-b4ef61104883
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_LISTENER_PROPERTY, WS_LISTENER_PROPERTY structure [Web Services for Windows], _WS_LISTENER_PROPERTY, webservices/WS_LISTENER_PROPERTY, wsw.ws_listener_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: WS_LISTENER_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_LISTENER_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_LISTENER_PROPERTY structure


## -description



                Specifies a listener specific setting.
            


## -struct-fields




### -field id


                Identifies the <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_ID</a>.
            


### -field value


                A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize


                The size, in bytes, of the memory pointed to by value.
            

