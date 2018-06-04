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

# _HTTP_AUTHENTICATION_HARDENING_LEVELS enumeration


## -description


Server Hardening level.


## -enum-fields




### -field HttpAuthenticationHardeningLegacy

Server is not hardened and operates without Channel Binding Token (CBT) support. 


### -field HttpAuthenticationHardeningMedium

Server is partially hardened.  Clients that support CBT are serviced appropriately.  Legacy clients are also serviced.


### -field HttpAuthenticationHardeningStrict

Server is hardened.  Only clients that supported CBT are serviced.

