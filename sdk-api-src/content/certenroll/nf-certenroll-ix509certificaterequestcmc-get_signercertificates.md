---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SignerCertificates
title: IX509CertificateRequestCmc::get_SignerCertificates
author: windows-sdk-content
description: Retrieves a collection of certificates used to sign the request.
old-location: security\ix509certificaterequestcmc_signercertificates_property.htm
old-project: seccertenroll
ms.assetid: 0b963fe2-32bd-4f99-9d4f-b17cb2d65909
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SignerCertificates property, IX509CertificateRequestCmc.SignerCertificates, IX509CertificateRequestCmc.get_SignerCertificates, IX509CertificateRequestCmc::SignerCertificates, IX509CertificateRequestCmc::get_SignerCertificates, SignerCertificates property [Security], SignerCertificates property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SignerCertificates, certenroll/IX509CertificateRequestCmc::get_SignerCertificates, get_SignerCertificates, security.ix509certificaterequestcmc_signercertificates_property
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
 - IX509CertificateRequestCmc.SignerCertificates
 - IX509CertificateRequestCmc.get_SignerCertificates
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::get_SignerCertificates


## -description


The <b>SignerCertificates</b> property retrieves a collection of certificates used to sign the request.

This property is read-only.


## -parameters


## -remarks



A CMC request can have a primary signature plus zero or more certificate-based signatures. Certificate-based signatures can be included in a request if, for example, one or more additional parties must vouch for the identity of the entity requesting the new certificate. Call the <b>SignerCertificates</b> property to retrieve a collection of these additional certificate-based signatures.

The primary signature is typically created by using the private key that matches the public key in the inner PKCS #10 request object. Because the private key is usually created to enroll a new request in a certificate hierarchy, the primary signature is not certificate-based, and you must call the <a href="https://msdn.microsoft.com/cd5353b4-b1dd-495f-ae75-c6e14edbb8f9">SignatureInformation</a> property to retrieve it.

You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
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
 

 

