---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MI_DestinationOptions_AddProxyCredentials function


## -description


Adds credentials to authenticate against a proxy.


## -parameters




### -param options [in, out]

A pointer to a destination options structure.


### -param credentials [in]

Credentials used when communicating with the destination machine.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Not all protocol transports support proxy configuration.  Not all proxy servers support all authentication types.  If the proxy requires dual-factor authentication this function can be called with both sets of credentials.



