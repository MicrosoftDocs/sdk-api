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

# _EAPHOST_AUTH_INFO structure


## -description


 The <b>EAPHOST_AUTH_INFO</b> structure describes current authentication information throughout different stages of the EAP authentication process.


## -struct-fields




### -field status

An <a href="https://msdn.microsoft.com/e1d0ff30-955c-4998-ae01-5dbadf3f4123">EAPHOST_AUTH_STATUS</a> enumeration value that specifies the current status of the authentication session.


### -field dwErrorCode

An error value, either from winerror.h or elsewhere (Raserror.h), that indicates the last error raised during the authentication process.


### -field dwReasonCode

A reason code that specifies the reason the error in <b>dwErrorCode</b> was raised. 


## -see-also




<a href="https://msdn.microsoft.com/77595f36-140d-4d8e-af8e-63e9de0031c4">EAPHost Supplicant Structures</a>



<a href="https://msdn.microsoft.com/adbb08d7-36a0-4e10-b0bc-2fb7030c2fcc">EapHostPeerAuthParams</a>



<a href="https://msdn.microsoft.com/cb5ceffb-941f-48ad-9271-111f41adc65b">EapHostPeerGetAuthStatus</a>
 

 

