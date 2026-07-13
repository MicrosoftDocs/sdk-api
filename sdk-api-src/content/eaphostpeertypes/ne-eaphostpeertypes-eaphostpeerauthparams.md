---
UID: NE:eaphostpeertypes.tagEapHostPeerAuthParams
title: EapHostPeerAuthParams (eaphostpeertypes.h)
description: Defines the set of possible authentication parameter values.
helpviewer_keywords: ["EapHostNapInfo","EapHostPeerAuthParams","EapHostPeerAuthParams enumeration [EAPHost]","EapHostPeerAuthStatus","EapHostPeerIdentity","EapHostPeerIdentityExtendedInfo","eaphost.eaphostpeerauthparams","eaphostpeertypes/EapHostNapInfo","eaphostpeertypes/EapHostPeerAuthParams","eaphostpeertypes/EapHostPeerAuthStatus","eaphostpeertypes/EapHostPeerIdentity","eaphostpeertypes/EapHostPeerIdentityExtendedInfo"]
old-location: eaphost\eaphostpeerauthparams.htm
tech.root: eaphost
ms.assetid: adbb08d7-36a0-4e10-b0bc-2fb7030c2fcc
ms.date: 12/05/2018
ms.keywords: EapHostNapInfo, EapHostPeerAuthParams, EapHostPeerAuthParams enumeration [EAPHost], EapHostPeerAuthStatus, EapHostPeerIdentity, EapHostPeerIdentityExtendedInfo, eaphost.eaphostpeerauthparams, eaphostpeertypes/EapHostNapInfo, eaphostpeertypes/EapHostPeerAuthParams, eaphostpeertypes/EapHostPeerAuthStatus, eaphostpeertypes/EapHostPeerIdentity, eaphostpeertypes/EapHostPeerIdentityExtendedInfo
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
req.typenames: EapHostPeerAuthParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEapHostPeerAuthParams
 - eaphostpeertypes/tagEapHostPeerAuthParams
 - EapHostPeerAuthParams
 - eaphostpeertypes/EapHostPeerAuthParams
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
 - EapHostPeerAuthParams
---

# EapHostPeerAuthParams enumeration


## -description

Defines the set of possible authentication parameter values.

## -enum-fields

### -field EapHostPeerAuthStatus:1

Contains the current status of authentication for the supplicant.

### -field EapHostPeerIdentity

Contains the user identity of the supplicant.

### -field EapHostPeerIdentityExtendedInfo

Contains extended user identity information for the supplicant from the identity packet.

### -field EapHostNapInfo

Windows 7 or later: Contains NAP-related information for the supplicant in an [EapHostPeerNapInfo](/windows/win32/eaphost/eaphostpeernapinfo) structure.

### -field v1_enum

## -see-also

[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus">EapHostPeerGetAuthStatus</a>
