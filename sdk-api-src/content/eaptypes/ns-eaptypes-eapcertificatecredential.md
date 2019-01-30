---
UID: NS:eaptypes._EapCertificateCredential
title: EapCertificateCredential
author: windows-sdk-content
description: Contains information about the certificate that the EAP method uses for authentication.
old-location: eaphost\eapcertificatecredential.htm
tech.root: eaphost
ms.assetid: 575967F4-E5CC-433D-919D-258B5849A5B1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EapCertificateCredential, EapCertificateCredential structure [EAPHost], eaphost.eapcertificatecredential, eaptypes/EapCertificateCredential
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - eaptypes.h
api_name:
 - EapCertificateCredential
product: Windows
targetos: Windows
req.typenames: EapCertificateCredential
req.redist: 
---

# EapCertificateCredential structure


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
 

 

