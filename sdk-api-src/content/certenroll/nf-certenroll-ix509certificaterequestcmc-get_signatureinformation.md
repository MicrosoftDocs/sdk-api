---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SignatureInformation
title: IX509CertificateRequestCmc::get_SignatureInformation (certenroll.h)
author: windows-sdk-content
description: Retrieves the IX509SignatureInformation object that contains information about the primary signature used to sign the certificate request.
old-location: security\ix509certificaterequestcmc_signatureinformation_property.htm
tech.root: seccertenroll
ms.assetid: cd5353b4-b1dd-495f-ae75-c6e14edbb8f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SignatureInformation property, IX509CertificateRequestCmc.SignatureInformation, IX509CertificateRequestCmc.get_SignatureInformation, IX509CertificateRequestCmc::SignatureInformation, IX509CertificateRequestCmc::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SignatureInformation, certenroll/IX509CertificateRequestCmc::get_SignatureInformation, get_SignatureInformation, security.ix509certificaterequestcmc_signatureinformation_property
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestCmc.SignatureInformation
 - IX509CertificateRequestCmc.get_SignatureInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::get_SignatureInformation


## -description


The <b>SignatureInformation</b> property retrieves the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object that contains information about the primary signature used to sign the certificate request. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object contains information about the hash, public key and signature algorithms used for the primary signature that signs the certificate request. A CMC request can have a primary signature plus zero or more certificate-based signatures. Certificate-based signatures can be included in a request if, for example, one or more additional parties must vouch for the identity of the entity requesting the new certificate. You can call the <a href="https://msdn.microsoft.com/0b963fe2-32bd-4f99-9d4f-b17cb2d65909">SignerCertificates</a> property to retrieve a collection of these additional certificate-based signatures.

The primary signature is typically created by using the private key that matches the public key in the inner PKCS #10 request object. Because the private key is usually created to enroll a new request in a certificate hierarchy, the primary signature is not certificate-based, and you must call the <b>SignatureInformation</b> property to retrieve it.

 If the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object does not exist when the <b>SignatureInformation</b> property is called or creation of the signature was deferred during initialization, this property:<ul>
<li>Retrieves the innermost PKCS #10 request object.</li>
<li>Retrieves and duplicates the signature information from the inner request.</li>
<li>Attempts to retrieve the private key associated with the inner PKCS #10 and sets the <a href="https://msdn.microsoft.com/99cefeed-caec-401e-bdcd-d167472b2cbd">NullSigned</a> property if no private key can be found.</li>
<li>Retrieves the hash algorithm, if one is specified, from the template associated with the inner request and sets the <a href="https://msdn.microsoft.com/b5242975-50e5-49d6-be1f-3a09ada03593">HashAlgorithm</a> property.</li>
<li>Retrieves the asymmetric algorithm, if one is specified, from the private key associated with the inner request and sets the <a href="https://msdn.microsoft.com/f964328f-15a6-4d8e-a2cf-73c8d74995e8">PublicKeyAlgorithm</a> property.</li>
<li>Retrieves the private key flags from the template and sets the <a href="https://msdn.microsoft.com/e62ecdf1-56d8-4707-8e5d-deef4d79a34c">AlternateSignatureAlgorithm</a> if appropriate </li>
</ul>


You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
<li>
<a href="https://msdn.microsoft.com/be0e2cda-5481-49ab-9a12-6dc52981fd24">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/40084cb0-eb48-485d-aa45-8ddb577f2d4f">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7500b714-4608-4da6-85ad-20cea30853cc">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b63bfaaa-a8af-4c72-a191-447230adae72">InitializeFromInnerRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/abf7617e-1194-4303-a214-23fbaf20eccf">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d6c15fcb-1883-4d87-af29-721102676535">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

