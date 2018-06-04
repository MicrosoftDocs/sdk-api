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

# _EAPHOST_AUTH_STATUS enumeration


## -description


Defines the set of possible EAP authentication session status values during the authentication process.


## -enum-fields




### -field EapHostInvalidSession

The EAP authentication session is no longer valid.


### -field EapHostAuthNotStarted

The authentication session has not started yet.


### -field EapHostAuthIdentityExchange

The supplicant is providing a user identity in order to begin the EAP authentication session.


### -field EapHostAuthNegotiatingType

The supplicant is negotiating the EAP method type to use for authentication.


### -field EapHostAuthInProgress

The authentication session is in progress.


### -field EapHostAuthSucceeded

The EAP authentication session completed successfully, and authentication was successful.


### -field EapHostAuthFailed

The EAP authentication session completed successfully, but authentication failed.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/b05a1862-9709-4459-a445-5ea4e00cab88">EAPHOST_AUTH_INFO</a>



<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>



<a href="https://msdn.microsoft.com/adbb08d7-36a0-4e10-b0bc-2fb7030c2fcc">EapHostPeerAuthParams</a>



<a href="https://msdn.microsoft.com/cb5ceffb-941f-48ad-9271-111f41adc65b">EapHostPeerGetAuthStatus</a>
 

 

