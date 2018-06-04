---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagEapPeerMethodResponseAction enumeration


## -description


Defines the set of actions an EAP authenticator can indicate to a supplicant or EAP peer method during authentication.


## -enum-fields




### -field EapPeerMethodResponseActionDiscard

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




<a href="https://msdn.microsoft.com/e57e8c74-b224-4c01-913b-e41af651acc3">EAPHost Peer Method Enumerations</a>
 

 

