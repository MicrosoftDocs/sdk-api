---
UID: NS:webservices._WS_SECURITY_ALGORITHM_PROPERTY
title: "_WS_SECURITY_ALGORITHM_PROPERTY"
author: windows-sdk-content
description: Specifies a cryptographic algorithm setting.
old-location: wsw\ws_security_algorithm_property.htm
tech.root: wsw
ms.assetid: 6a0dbe45-65f6-41eb-aa94-5ed0cdd751cf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_SECURITY_ALGORITHM_PROPERTY, WS_SECURITY_ALGORITHM_PROPERTY structure [Web Services for Windows], _WS_SECURITY_ALGORITHM_PROPERTY, webservices/WS_SECURITY_ALGORITHM_PROPERTY, wsw.ws_security_algorithm_property
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
 - WS_SECURITY_ALGORITHM_PROPERTY
product: Windows
targetos: Windows
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY
req.redist: 
---

# _WS_SECURITY_ALGORITHM_PROPERTY structure


## -description


Specifies a cryptographic algorithm setting.
            


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/eef63792-9dc6-49f5-bca3-e8056d0750f3">WS_SECURITY_ALGORITHM_PROPERTY_ID</a>.
            


### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize

The size in bytes of the memory pointed to by value.
            

