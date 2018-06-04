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

# __MIDL_IWTSSBPlugin_0009 structure


## -description


Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).


## -struct-fields




### -field wszUserName

The user name that is associated with the session. The name cannot exceed 104 characters.


### -field wszDomainName

The domain name of the user. The name cannot exceed 256 characters.


### -field ApplicationType

The name of the program that should be run after the session is created. The name cannot exceed 256 characters.


### -field dwSessionId

The session identifier.


### -field CreateTime

The time that the session was initiated.


### -field DisconnectTime

The time that the user disconnected from the session.


### -field SessionState

A value of the <a href="https://msdn.microsoft.com/d31118c5-56a3-4792-83fd-fdd3cd7a79ea">WTSSBX_SESSION_STATE</a> enumeration type that indicates the state of the session.


## -see-also




<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

