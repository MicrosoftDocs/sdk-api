---
UID: NE:eapauthenticatoractiondefine.tagEapPeerMethodResultReason
title: EapPeerMethodResultReason (eapauthenticatoractiondefine.h)
description: Defines the set of results of an EAP authentication session returned by an EAP authenticator method to an EAP peer method.
helpviewer_keywords: ["EapPeerMethodResultFailure","EapPeerMethodResultReason","EapPeerMethodResultReason enumeration [EAPHost]","EapPeerMethodResultReasonOle","EapPeerMethodResultSuccess","EapPeerMethodResultUnknown","eapauthenticatoractiondefine/EapPeerMethodResultFailure","eapauthenticatoractiondefine/EapPeerMethodResultReason","eapauthenticatoractiondefine/EapPeerMethodResultSuccess","eapauthenticatoractiondefine/EapPeerMethodResultUnknown","eaphost.eappeermethodresultreason"]
old-location: eaphost\eappeermethodresultreason.htm
tech.root: eaphost
ms.assetid: 5f7f18cd-cc75-4d13-a0c0-c60f8c5f1a07
ms.date: 12/05/2018
ms.keywords: EapPeerMethodResultFailure, EapPeerMethodResultReason, EapPeerMethodResultReason enumeration [EAPHost], EapPeerMethodResultReasonOle, EapPeerMethodResultSuccess, EapPeerMethodResultUnknown, eapauthenticatoractiondefine/EapPeerMethodResultFailure, eapauthenticatoractiondefine/EapPeerMethodResultReason, eapauthenticatoractiondefine/EapPeerMethodResultSuccess, eapauthenticatoractiondefine/EapPeerMethodResultUnknown, eaphost.eappeermethodresultreason
f1_keywords:
- eapauthenticatoractiondefine/EapPeerMethodResultReason
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- EapAuthenticatorActionDefine.h
api_name:
- EapPeerMethodResultReason
targetos: Windows
req.typenames: EapPeerMethodResultReason, EapPeerMethodResultReasonOle
req.redist: 
ms.custom: 19H1
---

# EapPeerMethodResultReason enumeration


## -description


Defines the set of results of an EAP authentication session returned by an EAP authenticator method to an EAP peer method.


## -enum-fields




### -field EapPeerMethodResultUnknown

The success or failure of the authentication session is unknown or indeterminate.


### -field EapPeerMethodResultSuccess

Authentication was successful.


### -field EapPeerMethodResultFailure

Authentication failed.


### -field v1_enum




## -remarks



<b>EapPeerMethodResultReason</b> includes <a href="https://docs.microsoft.com/windows/desktop/NLA/portal">network awareness</a> information for wireless devices.




## -see-also




[EAPHost Peer Method Enumerations](/windows/win32/eaphost/eap-host-peer-method-enumerations)
 

 

