---
UID: NE:eaphostpeertypes.tagEapHostPeerResponseAction
title: EapHostPeerResponseAction (eaphostpeertypes.h)
author: windows-sdk-content
description: Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.
old-location: eaphost\eaphostpeerresponseaction.htm
tech.root: eaphost
ms.assetid: 59bf6e02-90b5-4f9a-9865-b71852c61db9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerResponseAction, EapHostPeerResponseAction enumeration [EAPHost], EapHostPeerResponseDiscard, EapHostPeerResponseInvokeUI, EapHostPeerResponseNone, EapHostPeerResponseRespond, EapHostPeerResponseResult, EapHostPeerResponseSend, EapHostPeerResponseStartAuthentication, eaphost.eaphostpeerresponseaction, eaphostpeertypes/EapHostPeerResponseAction, eaphostpeertypes/EapHostPeerResponseDiscard, eaphostpeertypes/EapHostPeerResponseInvokeUI, eaphostpeertypes/EapHostPeerResponseNone, eaphostpeertypes/EapHostPeerResponseRespond, eaphostpeertypes/EapHostPeerResponseResult, eaphostpeertypes/EapHostPeerResponseSend, eaphostpeertypes/EapHostPeerResponseStartAuthentication
ms.topic: enum
f1_keywords: ["eaphostpeertypes/EapHostPeerResponseAction"]
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
 - EapHostPeerResponseAction
product: Windows
targetos: Windows
req.typenames: EapHostPeerResponseAction
req.redist: 
ms.custom: 19H1
---

# EapHostPeerResponseAction enumeration


## -description


Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.


## -enum-fields




### -field EapHostPeerResponseDiscard

The supplicant should discard the request as it is not usable by EAP.


### -field EapHostPeerResponseSend

The supplicant should send the indicated packet to the authenticator.


### -field EapHostPeerResponseResult

The supplicant should act on EAP attributes returned by the EAP authenticator.


### -field EapHostPeerResponseInvokeUi


### -field EapHostPeerResponseRespond

The supplicant should generate a  context-specific response to the EAP authenticator request.


### -field EapHostPeerResponseStartAuthentication

The EAPHost has started authentication.


### -field EapHostPeerResponseNone

The supplicant should generate no  response to the EAP authenticator request.


### -field v1_enum




#### - EapHostPeerResponseInvokeUI

The supplicant should invoke a user interface dialog on the client.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-enumerations">EAPHost Supplicant Enumerations</a>
 

 

