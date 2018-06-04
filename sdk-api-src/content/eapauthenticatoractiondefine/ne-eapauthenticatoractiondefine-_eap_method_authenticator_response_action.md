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

# _EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION enumeration


## -description


Defines the set of response instructions sent by the  authenticator to the supplicant or EAP peer method.


## -enum-fields




### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_DISCARD

The supplicant should discard the response as it is not usable by EAPHost.


### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_SEND

The supplicant should send the indicated packet to the authenticator.


### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_RESULT

The supplicant should act on EAP attributes returned by the authenticator.


### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_RESPOND

The supplicant should generate a  context-specific response to the authenticator request.


### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_AUTHENTICATE

The authenticator method has started authentication of the supplicant.


### -field EAP_METHOD_AUTHENTICATOR_RESPONSE_HANDLE_IDENTITY

The peer method should return the handle for the user identity of the supplicant.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/8c21625f-a9b7-4ea5-98ff-cdcce637dad8">EAP Host Authenticator Method Enumerations</a>
 

 

