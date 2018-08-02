---
UID: NS:webservices._WS_ERROR_PROPERTY
title: "_WS_ERROR_PROPERTY"
author: windows-sdk-content
description: Specifies an error specific setting.
old-location: wsw\ws_error_property.htm
old-project: wsw
ms.assetid: 463b634f-bb15-494d-8061-c4fa0b97b990
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_ERROR_PROPERTY, WS_ERROR_PROPERTY structure [Web Services for Windows], _WS_ERROR_PROPERTY, webservices/WS_ERROR_PROPERTY, wsw.ws_error_property
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
req.typenames: WS_ERROR_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ERROR_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_ERROR_PROPERTY structure


## -description


Specifies an error specific setting.
            


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/527e39be-c959-40db-8f0b-14dcd49a7ca7">WS_ERROR_PROPERTY_ID</a>.
            


### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size, in bytes, of the memory pointed to by value.
            

