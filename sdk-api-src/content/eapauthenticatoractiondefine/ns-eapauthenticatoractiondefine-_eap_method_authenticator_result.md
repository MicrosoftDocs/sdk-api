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

# _EAP_METHOD_AUTHENTICATOR_RESULT structure


## -description


Contains authentication results returned by an EAP authenticator method.


## -struct-fields




### -field fIsSuccess

If <b>TRUE</b>, the supplicant was successfully authenticated; if <b>FALSE</b>, it was not.


### -field dwFailureReason

Contains a reason code if the supplicant could not be authenticated. Reason codes are generally expected to originate from winerror.h.


### -field pAuthAttribs

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a> structure that contains the EAP attributes  returned by the authentication session.


## -see-also




<a href="https://msdn.microsoft.com/e26d5db7-f247-4bff-ae5f-081474f8e61e">EAPHost Authenticator Method Structures</a>
 

 

