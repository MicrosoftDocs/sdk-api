---
UID: NS:webservices._WS_SERVICE_PROPERTY
title: "_WS_SERVICE_PROPERTY"
author: windows-sdk-content
description: Specifies a service specific setting.
old-location: wsw\ws_service_property.htm
old-project: wsw
ms.assetid: d25cab25-2227-4afe-ae45-93a229d7f78b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_SERVICE_PROPERTY, WS_SERVICE_PROPERTY structure [Web Services for Windows], _WS_SERVICE_PROPERTY, webservices/WS_SERVICE_PROPERTY, wsw.ws_service_property
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
tech.root: 
req.typenames: WS_SERVICE_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SERVICE_PROPERTY structure


## -description


Specifies a service specific setting.
            


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/305fe7ad-e4a2-499a-b34b-e5b7cde53e22">WS_SERVICE_PROPERTY_ID</a>.
            


### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size, in bytes, of the memory pointed to by value.
            

