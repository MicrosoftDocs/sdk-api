---
UID: NE:eapauthenticatoractiondefine.tagEapPeerMethodResponseAction
title: EapPeerMethodResponseAction (eapauthenticatoractiondefine.h)
description: Defines the set of actions an EAP authenticator can indicate to a supplicant or EAP peer method during authentication.
helpviewer_keywords: ["EapPeerMethodResponseAction","EapPeerMethodResponseAction enumeration [EAPHost]","EapPeerMethodResponseActionDiscard","EapPeerMethodResponseActionInvokeUI","EapPeerMethodResponseActionNone","EapPeerMethodResponseActionRespond","EapPeerMethodResponseActionResult","EapPeerMethodResponseActionSend","eapauthenticatoractiondefine/EapPeerMethodResponseAction","eapauthenticatoractiondefine/EapPeerMethodResponseActionDiscard","eapauthenticatoractiondefine/EapPeerMethodResponseActionInvokeUI","eapauthenticatoractiondefine/EapPeerMethodResponseActionNone","eapauthenticatoractiondefine/EapPeerMethodResponseActionRespond","eapauthenticatoractiondefine/EapPeerMethodResponseActionResult","eapauthenticatoractiondefine/EapPeerMethodResponseActionSend","eaphost.eappeermethodresponseaction"]
old-location: eaphost\eappeermethodresponseaction.htm
tech.root: eaphost
ms.assetid: def7e04e-ed0c-46f0-97d6-4c0ab021fa8b
ms.date: 12/05/2018
ms.keywords: EapPeerMethodResponseAction, EapPeerMethodResponseAction enumeration [EAPHost], EapPeerMethodResponseActionDiscard, EapPeerMethodResponseActionInvokeUI, EapPeerMethodResponseActionNone, EapPeerMethodResponseActionRespond, EapPeerMethodResponseActionResult, EapPeerMethodResponseActionSend, eapauthenticatoractiondefine/EapPeerMethodResponseAction, eapauthenticatoractiondefine/EapPeerMethodResponseActionDiscard, eapauthenticatoractiondefine/EapPeerMethodResponseActionInvokeUI, eapauthenticatoractiondefine/EapPeerMethodResponseActionNone, eapauthenticatoractiondefine/EapPeerMethodResponseActionRespond, eapauthenticatoractiondefine/EapPeerMethodResponseActionResult, eapauthenticatoractiondefine/EapPeerMethodResponseActionSend, eaphost.eappeermethodresponseaction
req.header: eapauthenticatoractiondefine.h
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
req.typenames: EapPeerMethodResponseAction
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEapPeerMethodResponseAction
 - eapauthenticatoractiondefine/tagEapPeerMethodResponseAction
 - EapPeerMethodResponseAction
 - eapauthenticatoractiondefine/EapPeerMethodResponseAction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapAuthenticatorActionDefine.h
api_name:
 - EapPeerMethodResponseAction
---

# EapPeerMethodResponseAction enumeration


## -description

Defines the set of actions an EAP authenticator can indicate to a supplicant or EAP peer method during authentication.

## -enum-fields

### -field EapPeerMethodResponseActionDiscard:0

The supplicant should discard the request as it is not usable by EAP.

### -field EapPeerMethodResponseActionSend

The supplicant should send the indicated packet to the authenticator.

### -field EapPeerMethodResponseActionResult

The supplicant should act on EAP attributes returned by the EAP authenticator.

### -field EapPeerMethodResponseActionInvokeUI

The EAP peer method should invoke a user interface dialog on the client.

### -field EapPeerMethodResponseActionRespond

The supplicant should generate a  context-specific response to the EAP authenticator request.

### -field EapPeerMethodResponseActionNone

The supplicant should generate no  response to the EAP authenticator request.

### -field v1_enum

## -see-also

[EAPHost Peer Method Enumerations](/windows/win32/eaphost/eap-host-peer-method-enumerations)

