---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_OldCertificate
title: IX509CertificateRequestPkcs10::get_OldCertificate
author: windows-sdk-content
description: Retrieves the certificate passed to the InitializeFromCertificate method.
old-location: security\ix509certificaterequestpkcs10_oldcertificate_property.htm
old-project: SecCertEnroll
ms.assetid: 8bb15b5c-e642-477d-bcec-772748e336ef
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],OldCertificate property, IX509CertificateRequestPkcs10.OldCertificate, IX509CertificateRequestPkcs10.get_OldCertificate, IX509CertificateRequestPkcs10::OldCertificate, IX509CertificateRequestPkcs10::get_OldCertificate, OldCertificate property [Security], OldCertificate property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::OldCertificate, certenroll/IX509CertificateRequestPkcs10::get_OldCertificate, get_OldCertificate, security.ix509certificaterequestpkcs10_oldcertificate_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestPkcs10.OldCertificate
-	IX509CertificateRequestPkcs10.get_OldCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_OldCertificate


## -description


The <b>OldCertificate</b> property retrieves the certificate passed to the <a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a> method.  The certificate is contained in a byte array encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read-only.


## -parameters


## -remarks



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
 

 

