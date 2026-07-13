---
UID: NE:eaphostpeertypes.tagEapHostPeerResponseAction
title: EapHostPeerResponseAction (eaphostpeertypes.h)
description: Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.
helpviewer_keywords: ["EapHostPeerResponseAction","EapHostPeerResponseAction enumeration [EAPHost]","EapHostPeerResponseDiscard","EapHostPeerResponseInvokeUI","EapHostPeerResponseNone","EapHostPeerResponseRespond","EapHostPeerResponseResult","EapHostPeerResponseSend","EapHostPeerResponseStartAuthentication","eaphost.eaphostpeerresponseaction","eaphostpeertypes/EapHostPeerResponseAction","eaphostpeertypes/EapHostPeerResponseDiscard","eaphostpeertypes/EapHostPeerResponseInvokeUI","eaphostpeertypes/EapHostPeerResponseNone","eaphostpeertypes/EapHostPeerResponseRespond","eaphostpeertypes/EapHostPeerResponseResult","eaphostpeertypes/EapHostPeerResponseSend","eaphostpeertypes/EapHostPeerResponseStartAuthentication"]
old-location: eaphost\eaphostpeerresponseaction.htm
tech.root: eaphost
ms.assetid: 59bf6e02-90b5-4f9a-9865-b71852c61db9
ms.date: 12/05/2018
ms.keywords: EapHostPeerResponseAction, EapHostPeerResponseAction enumeration [EAPHost], EapHostPeerResponseDiscard, EapHostPeerResponseInvokeUI, EapHostPeerResponseNone, EapHostPeerResponseRespond, EapHostPeerResponseResult, EapHostPeerResponseSend, EapHostPeerResponseStartAuthentication, eaphost.eaphostpeerresponseaction, eaphostpeertypes/EapHostPeerResponseAction, eaphostpeertypes/EapHostPeerResponseDiscard, eaphostpeertypes/EapHostPeerResponseInvokeUI, eaphostpeertypes/EapHostPeerResponseNone, eaphostpeertypes/EapHostPeerResponseRespond, eaphostpeertypes/EapHostPeerResponseResult, eaphostpeertypes/EapHostPeerResponseSend, eaphostpeertypes/EapHostPeerResponseStartAuthentication
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
req.typenames: EapHostPeerResponseAction
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEapHostPeerResponseAction
 - eaphostpeertypes/tagEapHostPeerResponseAction
 - EapHostPeerResponseAction
 - eaphostpeertypes/EapHostPeerResponseAction
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
 - EapHostPeerResponseAction
---

## -description

Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.

## -enum-fields

### -field EapHostPeerResponseDiscard:0

The supplicant should discard the request as it is not usable by EAP.

### -field EapHostPeerResponseSend

The supplicant should send the indicated packet to the authenticator.

### -field EapHostPeerResponseResult

The supplicant should act on EAP attributes returned by the EAP authenticator.

### -field EapHostPeerResponseInvokeUi

The supplicant should invoke a user interface dialog on the client.

### -field EapHostPeerResponseRespond

The supplicant should generate a  context-specific response to the EAP authenticator request.

### -field EapHostPeerResponseStartAuthentication

The EAPHost has started authentication.

### -field EapHostPeerResponseNone

The supplicant should generate no  response to the EAP authenticator request.

## -see-also

[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)

