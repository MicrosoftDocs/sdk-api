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

# _EapCredentialType enumeration


## -description


The <b>EapCredentialType</b> enumeration defines the set of possible EAP credentials that can be passed to the <a href="https://msdn.microsoft.com/81817FAA-20AE-4556-BAA5-0EF2A955B6A3">EapPeerGetConfigBlobAndUserBlob</a> function.


## -enum-fields




### -field EAP_EMPTY_CREDENTIAL

The EAP method has no credential passed to it. The method must attempt a machine authentication.


### -field EAP_USERNAME_PASSWORD_CREDENTIAL

The EAP method uses a username and password for authentication. The credentials are passed using the <a href="https://msdn.microsoft.com/61484095-4354-4103-9E21-683002750B26">EapUsernamePasswordCredential</a> structure.


### -field EAP_WINLOGON_CREDENTIAL

The EAP method uses the logged-on user credentials for authentication.


### -field EAP_CERTIFICATE_CREDENTIAL

The EAP method uses a certificate present on the system for authentication. The credential is passed as an <a href="https://msdn.microsoft.com/575967F4-E5CC-433D-919D-258B5849A5B1">EapCertificateCredential</a> structure.


### -field EAP_SIM_CREDENTIAL

The EAP method uses a SIM for authentication. This is passed as an <a href="https://msdn.microsoft.com/483BF257-BB9F-4AF6-A55C-77277AC6E21F">EapSimCredential</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/575967F4-E5CC-433D-919D-258B5849A5B1">EapCertificateCredential</a>



<a href="https://msdn.microsoft.com/81817FAA-20AE-4556-BAA5-0EF2A955B6A3">EapPeerGetConfigBlobAndUserBlob</a>



<a href="https://msdn.microsoft.com/483BF257-BB9F-4AF6-A55C-77277AC6E21F">EapSimCredential</a>



<a href="https://msdn.microsoft.com/61484095-4354-4103-9E21-683002750B26">EapUsernamePasswordCredential</a>
 

 

