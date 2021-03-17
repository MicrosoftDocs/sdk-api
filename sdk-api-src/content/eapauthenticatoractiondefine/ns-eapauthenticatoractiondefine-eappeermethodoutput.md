---
UID: NS:eapauthenticatoractiondefine.tagEapPeerMethodOuput
title: EapPeerMethodOutput (eapauthenticatoractiondefine.h)
description: Contains the action information returned by an EAP peer method.
helpviewer_keywords: ["EapPeerMethodOutput","EapPeerMethodOutput structure [EAPHost]","eapauthenticatoractiondefine/EapPeerMethodOutput","eaphost.eappeermethodoutput"]
old-location: eaphost\eappeermethodoutput.htm
tech.root: eaphost
ms.assetid: fb3d423e-8509-4478-87d5-86bcbd90a8e7
ms.date: 12/05/2018
ms.keywords: EapPeerMethodOutput, EapPeerMethodOutput structure [EAPHost], eapauthenticatoractiondefine/EapPeerMethodOutput, eaphost.eappeermethodoutput
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
req.typenames: EapPeerMethodOutput
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEapPeerMethodOuput
 - eapauthenticatoractiondefine/tagEapPeerMethodOuput
 - EapPeerMethodOutput
 - eapauthenticatoractiondefine/EapPeerMethodOutput
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
 - EapPeerMethodOutput
---

# EapPeerMethodOutput structure


## -description

Contains the action information returned by an EAP peer method.

## -struct-fields

### -field action

<a href="/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction">EapPeerMethodResponseAction</a> enumeration value that indicates the response EAPHost should take as a result of the EAP peer method operation.

### -field fAllowNotifications

If <b>TRUE</b>, allows EAPHost to raise a notification to the user; otherwise, do not allow notifications.

## -see-also

[EAPHost Peer Method Structures](/windows/win32/eaphost/eap-host-peer-method-structures)

