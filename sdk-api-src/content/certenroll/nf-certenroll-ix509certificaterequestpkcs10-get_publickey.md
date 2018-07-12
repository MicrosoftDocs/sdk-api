---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_PublicKey
title: IX509CertificateRequestPkcs10::get_PublicKey
author: windows-sdk-content
description: Retrieves the IX509PublicKey object that contains the public key included in the certificate request.
old-location: security\ix509certificaterequestpkcs10_publickey_property.htm
old-project: seccertenroll
ms.assetid: 9f9d05d8-9bc5-441e-8409-498ee9d20c25
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],PublicKey property, IX509CertificateRequestPkcs10.PublicKey, IX509CertificateRequestPkcs10.get_PublicKey, IX509CertificateRequestPkcs10::PublicKey, IX509CertificateRequestPkcs10::get_PublicKey, PublicKey property [Security], PublicKey property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::PublicKey, certenroll/IX509CertificateRequestPkcs10::get_PublicKey, get_PublicKey, security.ix509certificaterequestpkcs10_publickey_property
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
 - IX509CertificateRequestPkcs10.PublicKey
 - IX509CertificateRequestPkcs10.get_PublicKey
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_PublicKey


## -description


The <b>PublicKey</b> property retrieves the <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> object that contains the public key included in the certificate request.

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
 

 

