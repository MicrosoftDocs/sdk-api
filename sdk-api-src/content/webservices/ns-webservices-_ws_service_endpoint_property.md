---
UID: NS:webservices._WS_SERVICE_ENDPOINT_PROPERTY
title: "_WS_SERVICE_ENDPOINT_PROPERTY"
author: windows-sdk-content
description: Specifies a service specific setting.
old-location: wsw\ws_service_endpoint_property.htm
old-project: wsw
ms.assetid: 4342d1d2-3126-401b-8019-c7dd243d4ac4
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_SERVICE_ENDPOINT_PROPERTY, WS_SERVICE_ENDPOINT_PROPERTY structure [Web Services for Windows], _WS_SERVICE_ENDPOINT_PROPERTY, webservices/WS_SERVICE_ENDPOINT_PROPERTY, wsw.ws_service_endpoint_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WS_SERVICE_ENDPOINT_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_ENDPOINT_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SERVICE_ENDPOINT_PROPERTY structure


## -description



                Specifies a service specific setting.
            


## -struct-fields




### -field id


                Identifies the <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_ID</a>.
            


### -field value


                A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize


                The size in bytes of the memory pointed to by value.
            

