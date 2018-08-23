---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_Subject
title: IX509CertificateRequestPkcs10::get_Subject
author: windows-sdk-content
description: Specifies or retrieves the X.500 distinguished name of the entity requesting the certificate.
old-location: security\ix509certificaterequestpkcs10_subject_property.htm
old-project: seccertenroll
ms.assetid: 7b521586-f2fc-4b2f-83ab-79f9b972f9a1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],Subject property, IX509CertificateRequestPkcs10.Subject, IX509CertificateRequestPkcs10.get_Subject, IX509CertificateRequestPkcs10::Subject, IX509CertificateRequestPkcs10::get_Subject, IX509CertificateRequestPkcs10::put_Subject, Subject property [Security], Subject property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::Subject, certenroll/IX509CertificateRequestPkcs10::get_Subject, certenroll/IX509CertificateRequestPkcs10::put_Subject, get_Subject, security.ix509certificaterequestpkcs10_subject_property
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
 - IX509CertificateRequestPkcs10.Subject
 - IX509CertificateRequestPkcs10.get_Subject
 - IX509CertificateRequestPkcs10.put_Subject
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_Subject


## -description


The <b>Subject</b> property specifies or retrieves the X.500 distinguished name of the entity requesting the certificate. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



You must set this property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, and you must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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
 

 

