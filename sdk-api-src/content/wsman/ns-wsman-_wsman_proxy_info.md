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

# _WSMAN_PROXY_INFO structure


## -description


Specifies proxy information.


## -struct-fields




### -field accessType

Specifies the access type for the proxy. This member must be set to one of the values defined in the <a href="https://msdn.microsoft.com/0c7d13dc-42e0-4c91-bcdf-c198b557206b">WSManProxyAccessType</a> enumeration.


### -field authenticationCredentials

A <a href="https://msdn.microsoft.com/e9090d88-c76e-4a85-946e-ff46403e6725">WSMAN_AUTHENTICATION_CREDENTIALS</a> structure that specifies the credentials and authentication scheme used for proxy access.

