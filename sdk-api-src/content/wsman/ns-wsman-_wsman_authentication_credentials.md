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

# _WSMAN_AUTHENTICATION_CREDENTIALS structure


## -description


Defines the authentication method and the credentials used for server or proxy authentication.


## -struct-fields




### -field authenticationMechanism

Defines the authentication mechanism. This member can be set to zero. If it is set to zero, the WinRM client will choose between Kerberos and Negotiate. If it is not set to zero, this member must be one of the values of the <a href="https://msdn.microsoft.com/ce5ddaf6-4d81-4dab-a928-819b1fdee6c8">WSManAuthenticationFlags</a> enumeration.


### -field userAccount

Defines the credentials used for authentication. See <a href="https://msdn.microsoft.com/5cb2b52f-85a7-4760-9f0d-b515fad86d33">WSMAN_USERNAME_PASSWORD_CREDS</a> for more information.


### -field certificateThumbprint

Defines the certificate thumbprint.

