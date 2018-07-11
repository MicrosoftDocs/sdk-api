---
UID: NE:eapauthenticatoractiondefine.tagEapPeerMethodResultReason
title: tagEapPeerMethodResultReason
author: windows-sdk-content
description: Defines the set of results of an EAP authentication session returned by an EAP authenticator method to an EAP peer method.
old-location: eaphost\eappeermethodresultreason.htm
old-project: eaphost
ms.assetid: 5f7f18cd-cc75-4d13-a0c0-c60f8c5f1a07
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: EapPeerMethodResultFailure, EapPeerMethodResultReason, EapPeerMethodResultReason enumeration [EAPHost], EapPeerMethodResultReasonOle, EapPeerMethodResultSuccess, EapPeerMethodResultUnknown, eapauthenticatoractiondefine/EapPeerMethodResultFailure, eapauthenticatoractiondefine/EapPeerMethodResultReason, eapauthenticatoractiondefine/EapPeerMethodResultSuccess, eapauthenticatoractiondefine/EapPeerMethodResultUnknown, eaphost.eappeermethodresultreason, tagEapPeerMethodResultReason
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: EapPeerMethodResultReason, EapPeerMethodResultReasonOle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapAuthenticatorActionDefine.h
api_name:
 - EapPeerMethodResultReason
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# tagEapPeerMethodResultReason enumeration


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



<b>EapPeerMethodResultReason</b> includes <a href="https://msdn.microsoft.com/a30741ff-5d9a-4ebb-8373-97e9116fc64b">network awareness</a> information for wireless devices.




## -see-also




<a href="https://msdn.microsoft.com/e57e8c74-b224-4c01-913b-e41af651acc3">EAPHost Peer Method Enumerations</a>
 

 

