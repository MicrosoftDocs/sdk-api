---
UID: NF:certenroll.IX509CertificateRequestPkcs7.get_SignerCertificate
title: IX509CertificateRequestPkcs7::get_SignerCertificate
author: windows-sdk-content
description: Specifies or retrieves a certificate used to sign the certificate request.
old-location: security\ix509certificaterequestpkcs7_signercertificate_property.htm
tech.root: SecCertEnroll
ms.assetid: 5d93aad0-6b93-4508-9bf0-82f673585ead
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequestPkcs7 interface [Security],SignerCertificate property, IX509CertificateRequestPkcs7.SignerCertificate, IX509CertificateRequestPkcs7.get_SignerCertificate, IX509CertificateRequestPkcs7::SignerCertificate, IX509CertificateRequestPkcs7::get_SignerCertificate, IX509CertificateRequestPkcs7::put_SignerCertificate, SignerCertificate property [Security], SignerCertificate property [Security],IX509CertificateRequestPkcs7 interface, certenroll/IX509CertificateRequestPkcs7::SignerCertificate, certenroll/IX509CertificateRequestPkcs7::get_SignerCertificate, certenroll/IX509CertificateRequestPkcs7::put_SignerCertificate, get_SignerCertificate, security.ix509certificaterequestpkcs7_signercertificate_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IX509CertificateRequestPkcs7.SignerCertificate
 - IX509CertificateRequestPkcs7.get_SignerCertificate
 - IX509CertificateRequestPkcs7.put_SignerCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs7::get_SignerCertificate


## -description


The <b>SignerCertificate</b> property specifies or retrieves a  certificate used to sign the certificate request.

This property is read/write.


## -parameters


## -remarks



You must initialize the PKCS #7 request object before calling this property. For more information, see the following topics:<ul>
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
<a href="https://msdn.microsoft.com/d6c15fcb-1883-4d87-af29-721102676535">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
 

 

