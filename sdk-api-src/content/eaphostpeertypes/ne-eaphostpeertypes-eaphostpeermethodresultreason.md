---
UID: NE:eaphostpeertypes.tagEapHostPeerMethodResultReason
title: EapHostPeerMethodResultReason (eaphostpeertypes.h)
description: Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.
helpviewer_keywords: ["EapHostPeerMethodResultAltSuccessReceived","EapHostPeerMethodResultFromMethod","EapHostPeerMethodResultReason","EapHostPeerMethodResultReason enumeration [EAPHost]","EapHostPeerMethodResultTimeout","eaphost.eaphostpeermethodresultreason","eaphostpeertypes/EapHostPeerMethodResultAltSuccessReceived","eaphostpeertypes/EapHostPeerMethodResultFromMethod","eaphostpeertypes/EapHostPeerMethodResultReason","eaphostpeertypes/EapHostPeerMethodResultTimeout"]
old-location: eaphost\eaphostpeermethodresultreason.htm
tech.root: eaphost
ms.assetid: f43d2883-d23f-455b-bde0-244a88630d25
ms.date: 12/05/2018
ms.keywords: EapHostPeerMethodResultAltSuccessReceived, EapHostPeerMethodResultFromMethod, EapHostPeerMethodResultReason, EapHostPeerMethodResultReason enumeration [EAPHost], EapHostPeerMethodResultTimeout, eaphost.eaphostpeermethodresultreason, eaphostpeertypes/EapHostPeerMethodResultAltSuccessReceived, eaphostpeertypes/EapHostPeerMethodResultFromMethod, eaphostpeertypes/EapHostPeerMethodResultReason, eaphostpeertypes/EapHostPeerMethodResultTimeout
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
req.typenames: EapHostPeerMethodResultReason
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEapHostPeerMethodResultReason
 - eaphostpeertypes/tagEapHostPeerMethodResultReason
 - EapHostPeerMethodResultReason
 - eaphostpeertypes/EapHostPeerMethodResultReason
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
 - EapHostPeerMethodResultReason
---

# EapHostPeerMethodResultReason enumeration


## -description

Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.

## -enum-fields

### -field EapHostPeerMethodResultAltSuccessReceived:1

Authentication was successful.

### -field EapHostPeerMethodResultTimeout

The method timed out waiting for a response.

### -field EapHostPeerMethodResultFromMethod

The  authentication process was completely normally.

### -field v1_enum

## -see-also

[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult">EapHostPeerGetResult</a>
