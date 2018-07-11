---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_SignatureInformation
title: IX509CertificateRequestPkcs10::get_SignatureInformation
author: windows-sdk-content
description: Retrieves the IX509SignatureInformation object that contains information about the certificate request signature.
old-location: security\ix509certificaterequestpkcs10_signatureinformation_property.htm
old-project: seccertenroll
ms.assetid: d90a8b82-a4d7-4d31-bcd0-293572a2bdd2
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],SignatureInformation property, IX509CertificateRequestPkcs10.SignatureInformation, IX509CertificateRequestPkcs10.get_SignatureInformation, IX509CertificateRequestPkcs10::SignatureInformation, IX509CertificateRequestPkcs10::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::SignatureInformation, certenroll/IX509CertificateRequestPkcs10::get_SignatureInformation, get_SignatureInformation, security.ix509certificaterequestpkcs10_signatureinformation_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
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
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestPkcs10.SignatureInformation
 - IX509CertificateRequestPkcs10.get_SignatureInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_SignatureInformation


## -description


The <b>SignatureInformation</b> property retrieves the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object that contains information about the certificate request signature. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object contains information about the hash, public key and signature algorithms used to sign the certificate request. If no <b>IX509SignatureInformation</b> object has been associated with the request, this property attempts to create one and use the private key to set the <a href="https://msdn.microsoft.com/f964328f-15a6-4d8e-a2cf-73c8d74995e8">PublicKeyAlgorithm</a> property.

 You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object and call  <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

