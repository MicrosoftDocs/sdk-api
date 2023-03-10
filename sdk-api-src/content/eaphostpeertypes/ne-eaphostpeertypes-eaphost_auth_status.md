---
UID: NE:eaphostpeertypes._EAPHOST_AUTH_STATUS
title: EAPHOST_AUTH_STATUS (eaphostpeertypes.h)
description: Defines the set of possible EAP authentication session status values during the authentication process.
helpviewer_keywords: ["EAPHOST_AUTH_STATUS","EAPHOST_AUTH_STATUS enumeration [EAPHost]","EapHostAuthFailed","EapHostAuthIdentityExchange","EapHostAuthInProgress","EapHostAuthNegotiatingType","EapHostAuthNotStarted","EapHostAuthSucceeded","EapHostInvalidSession","eaphost.eaphost_auth_status","eaphostpeertypes/EAPHOST_AUTH_STATUS","eaphostpeertypes/EapHostAuthFailed","eaphostpeertypes/EapHostAuthIdentityExchange","eaphostpeertypes/EapHostAuthInProgress","eaphostpeertypes/EapHostAuthNegotiatingType","eaphostpeertypes/EapHostAuthNotStarted","eaphostpeertypes/EapHostAuthSucceeded","eaphostpeertypes/EapHostInvalidSession"]
old-location: eaphost\eaphost_auth_status.htm
tech.root: eaphost
ms.assetid: e1d0ff30-955c-4998-ae01-5dbadf3f4123
ms.date: 12/05/2018
ms.keywords: EAPHOST_AUTH_STATUS, EAPHOST_AUTH_STATUS enumeration [EAPHost], EapHostAuthFailed, EapHostAuthIdentityExchange, EapHostAuthInProgress, EapHostAuthNegotiatingType, EapHostAuthNotStarted, EapHostAuthSucceeded, EapHostInvalidSession, eaphost.eaphost_auth_status, eaphostpeertypes/EAPHOST_AUTH_STATUS, eaphostpeertypes/EapHostAuthFailed, eaphostpeertypes/EapHostAuthIdentityExchange, eaphostpeertypes/EapHostAuthInProgress, eaphostpeertypes/EapHostAuthNegotiatingType, eaphostpeertypes/EapHostAuthNotStarted, eaphostpeertypes/EapHostAuthSucceeded, eaphostpeertypes/EapHostInvalidSession
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
targetos: Windows
req.typenames: EAPHOST_AUTH_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAPHOST_AUTH_STATUS
 - eaphostpeertypes/_EAPHOST_AUTH_STATUS
 - EAPHOST_AUTH_STATUS
 - eaphostpeertypes/EAPHOST_AUTH_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaphostpeertypes.h
api_name:
 - EAPHOST_AUTH_STATUS
---

# EAPHOST_AUTH_STATUS enumeration


## -description

Defines the set of possible EAP authentication session status values during the authentication process.

## -enum-fields

### -field EapHostInvalidSession:0

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

<a href="/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info">EAPHOST_AUTH_INFO</a>



[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)



<a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams">EapHostPeerAuthParams</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus">EapHostPeerGetAuthStatus</a>
