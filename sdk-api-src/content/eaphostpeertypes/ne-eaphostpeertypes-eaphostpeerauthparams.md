---
UID: NE:eaphostpeertypes.tagEapHostPeerAuthParams
title: EapHostPeerAuthParams (eaphostpeertypes.h)
author: windows-sdk-content
description: Defines the set of possible authentication parameter values.
old-location: eaphost\eaphostpeerauthparams.htm
tech.root: eaphost
ms.assetid: adbb08d7-36a0-4e10-b0bc-2fb7030c2fcc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostNapInfo, EapHostPeerAuthParams, EapHostPeerAuthParams enumeration [EAPHost], EapHostPeerAuthStatus, EapHostPeerIdentity, EapHostPeerIdentityExtendedInfo, eaphost.eaphostpeerauthparams, eaphostpeertypes/EapHostNapInfo, eaphostpeertypes/EapHostPeerAuthParams, eaphostpeertypes/EapHostPeerAuthStatus, eaphostpeertypes/EapHostPeerIdentity, eaphostpeertypes/EapHostPeerIdentityExtendedInfo
ms.topic: enum
f1_keywords: ["eaphostpeertypes/EapHostPeerAuthParams"]
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
 - EapHostPeerAuthParams
product: Windows
targetos: Windows
req.typenames: EapHostPeerAuthParams
req.redist: 
ms.custom: 19H1
---

# EapHostPeerAuthParams enumeration


## -description


Defines the set of possible authentication parameter values.


## -enum-fields




### -field EapHostPeerAuthStatus

Contains the current status of authentication for the supplicant.


### -field EapHostPeerIdentity

Contains the user identity of the supplicant.


### -field EapHostPeerIdentityExtendedInfo

Contains extended user identity information for the supplicant from the identity packet.


### -field EapHostNapInfo

Windows 7 or later: Contains NAP-related information for the supplicant in an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphostpeernapinfo">EapHostPeerNapInfo</a> structure.


### -field v1_enum




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-enumerations">EAPHost Supplicant Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus">EapHostPeerGetAuthStatus</a>
 

 

