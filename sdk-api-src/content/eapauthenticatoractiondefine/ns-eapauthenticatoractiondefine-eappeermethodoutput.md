---
UID: NS:eapauthenticatoractiondefine.tagEapPeerMethodOuput
title: EapPeerMethodOutput (eapauthenticatoractiondefine.h)
author: windows-sdk-content
description: Contains the action information returned by an EAP peer method.
old-location: eaphost\eappeermethodoutput.htm
tech.root: eaphost
ms.assetid: fb3d423e-8509-4478-87d5-86bcbd90a8e7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapPeerMethodOutput, EapPeerMethodOutput structure [EAPHost], eapauthenticatoractiondefine/EapPeerMethodOutput, eaphost.eappeermethodoutput
ms.topic: struct
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
 - EapPeerMethodOutput
product: Windows
targetos: Windows
req.typenames: EapPeerMethodOutput
req.redist: 
---

# EapPeerMethodOutput structure


## -description


Contains the action information returned by an EAP peer method.


## -struct-fields




### -field action


<a href="https://msdn.microsoft.com/en-us/library/Aa363618(v=VS.85).aspx">EapPeerMethodResponseAction</a> enumeration value that indicates the response EAPHost should take as a result of the EAP peer method operation.


### -field fAllowNotifications

If <b>TRUE</b>, allows EAPHost to raise a notification to the user; otherwise, do not allow notifications.


## -see-also




<a href="https://msdn.microsoft.com/546ef715-8f51-4f5a-a569-8bf64d52de85">EAPHost Peer Method Structures</a>
 

 

