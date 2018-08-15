---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_NullSigned
title: IX509CertificateRequestPkcs10::get_NullSigned
author: windows-sdk-content
description: Retrieves a Boolean value that indicates whether the certificate request is null-signed.
old-location: security\ix509certificaterequestpkcs10_nullsigned_property.htm
old-project: seccertenroll
ms.assetid: 2420f5ef-2cd7-498d-892a-2b99c524d629
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],NullSigned property, IX509CertificateRequestPkcs10.NullSigned, IX509CertificateRequestPkcs10.get_NullSigned, IX509CertificateRequestPkcs10::NullSigned, IX509CertificateRequestPkcs10::get_NullSigned, NullSigned property [Security], NullSigned property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::NullSigned, certenroll/IX509CertificateRequestPkcs10::get_NullSigned, get_NullSigned, security.ix509certificaterequestpkcs10_nullsigned_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - IX509CertificateRequestPkcs10.NullSigned
 - IX509CertificateRequestPkcs10.get_NullSigned
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_NullSigned


## -description


The <b>NullSigned</b> property retrieves a Boolean value that indicates whether the certificate request is null-signed.

This property is read-only.


## -parameters


## -remarks



A null-signed PKCS #10 certificate request is not really signed. That is, the signature is a hash created by using a digest algorithm such as SHA-1, but the request is not encrypted with a public key algorithm such as RSA. This can be used when a private key is not available as is often the case when <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authorities</a> are being cross-certified. For more information, see the <a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a> method.

 You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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
 

 

