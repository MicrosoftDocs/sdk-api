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

# tagEapHostPeerResponseAction enumeration


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




<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>
 

 

