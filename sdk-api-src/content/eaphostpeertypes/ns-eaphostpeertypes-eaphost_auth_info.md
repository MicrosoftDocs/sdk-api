---
UID: NS:eaphostpeertypes._EAPHOST_AUTH_INFO
title: EAPHOST_AUTH_INFO (eaphostpeertypes.h)
description: Describes current authentication information throughout different stages of the EAP authentication process.
helpviewer_keywords: ["EAPHOST_AUTH_INFO","EAPHOST_AUTH_INFO structure [EAPHost]","eaphost.eaphost_auth_info","eaphostpeertypes/EAPHOST_AUTH_INFO"]
old-location: eaphost\eaphost_auth_info.htm
tech.root: eaphost
ms.assetid: b05a1862-9709-4459-a445-5ea4e00cab88
ms.date: 12/05/2018
ms.keywords: EAPHOST_AUTH_INFO, EAPHOST_AUTH_INFO structure [EAPHost], eaphost.eaphost_auth_info, eaphostpeertypes/EAPHOST_AUTH_INFO
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
req.typenames: EAPHOST_AUTH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAPHOST_AUTH_INFO
 - eaphostpeertypes/_EAPHOST_AUTH_INFO
 - EAPHOST_AUTH_INFO
 - eaphostpeertypes/EAPHOST_AUTH_INFO
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
 - EAPHOST_AUTH_INFO
---

# EAPHOST_AUTH_INFO structure


## -description

 The <b>EAPHOST_AUTH_INFO</b> structure describes current authentication information throughout different stages of the EAP authentication process.

## -struct-fields

### -field status

An <a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphost_auth_status">EAPHOST_AUTH_STATUS</a> enumeration value that specifies the current status of the authentication session.

### -field dwErrorCode

An error value, either from winerror.h or elsewhere (Raserror.h), that indicates the last error raised during the authentication process.

### -field dwReasonCode

A reason code that specifies the reason the error in <b>dwErrorCode</b> was raised.

## -see-also

[EAPHost Supplicant Structures](/windows/win32/eaphost/eap-host-supplicant-structures)



<a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams">EapHostPeerAuthParams</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus">EapHostPeerGetAuthStatus</a>