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

# _EapCertificateCredential structure


## -description


The <b>EapCertificateCredential</b> structure contains information about the certificate that the EAP method uses for authentication.


## -struct-fields




### -field certHash

 


### -field password

If the certificate is present on the system and strong private key protection is turned on for this certificate, this field contains the password to access the certificate.


#### - certHash(CERTIFICATE_HASH_LENGTH)

SHA1 hash of the certificate.


## -see-also




<a href="https://msdn.microsoft.com/DC1B9524-2853-404D-A77A-61CB012FCF11">EapCredential</a>



<a href="https://msdn.microsoft.com/E77AA5E1-970A-43A6-916D-623A9C554F53">EapCredentialType</a>
 

 

