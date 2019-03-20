---
UID: NE:eaphostpeertypes._EAPHOST_AUTH_STATUS
title: EAPHOST_AUTH_STATUS (eaphostpeertypes.h)
author: windows-sdk-content
description: Defines the set of possible EAP authentication session status values during the authentication process.
old-location: eaphost\eaphost_auth_status.htm
tech.root: eaphost
ms.assetid: e1d0ff30-955c-4998-ae01-5dbadf3f4123
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EAPHOST_AUTH_STATUS, EAPHOST_AUTH_STATUS enumeration [EAPHost], EapHostAuthFailed, EapHostAuthIdentityExchange, EapHostAuthInProgress, EapHostAuthNegotiatingType, EapHostAuthNotStarted, EapHostAuthSucceeded, EapHostInvalidSession, eaphost.eaphost_auth_status, eaphostpeertypes/EAPHOST_AUTH_STATUS, eaphostpeertypes/EapHostAuthFailed, eaphostpeertypes/EapHostAuthIdentityExchange, eaphostpeertypes/EapHostAuthInProgress, eaphostpeertypes/EapHostAuthNegotiatingType, eaphostpeertypes/EapHostAuthNotStarted, eaphostpeertypes/EapHostAuthSucceeded, eaphostpeertypes/EapHostInvalidSession
ms.topic: enum
req.header: eaphostpeertypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - eaphostpeertypes.h
api_name:
 - EAPHOST_AUTH_STATUS
product: Windows
targetos: Windows
req.typenames: EAPHOST_AUTH_STATUS
req.redist: 
---

# EAPHOST_AUTH_STATUS enumeration


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




<a href="https://msdn.microsoft.com/en-us/library/Aa363582(v=VS.85).aspx">EAPHOST_AUTH_INFO</a>



<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363548(v=VS.85).aspx">EapHostPeerAuthParams</a>



<a href="https://msdn.microsoft.com/cb5ceffb-941f-48ad-9271-111f41adc65b">EapHostPeerGetAuthStatus</a>
 

 

