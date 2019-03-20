---
UID: NF:certenroll.IX509CertificateRequestPkcs7.get_RequesterName
title: IX509CertificateRequestPkcs7::get_RequesterName (certenroll.h)
author: windows-sdk-content
description: Specifies or retrieves a string that contains the Security Account Manager (SAM) name of the end-entity requesting the certificate.
old-location: security\ix509certificaterequestpkcs7_requestername_property.htm
tech.root: seccertenroll
ms.assetid: af85e976-cc79-4285-b553-a8001e84ec68
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509CertificateRequestPkcs7 interface [Security],RequesterName property, IX509CertificateRequestPkcs7.RequesterName, IX509CertificateRequestPkcs7.get_RequesterName, IX509CertificateRequestPkcs7::RequesterName, IX509CertificateRequestPkcs7::get_RequesterName, IX509CertificateRequestPkcs7::put_RequesterName, RequesterName property [Security], RequesterName property [Security],IX509CertificateRequestPkcs7 interface, certenroll/IX509CertificateRequestPkcs7::RequesterName, certenroll/IX509CertificateRequestPkcs7::get_RequesterName, certenroll/IX509CertificateRequestPkcs7::put_RequesterName, get_RequesterName, security.ix509certificaterequestpkcs7_requestername_property
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
 - IX509CertificateRequestPkcs7.RequesterName
 - IX509CertificateRequestPkcs7.get_RequesterName
 - IX509CertificateRequestPkcs7.put_RequesterName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs7::get_RequesterName


## -description


The <b>RequesterName</b> property specifies or retrieves a string that contains the Security Account Manager (SAM) name of the end-entity requesting the certificate. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



This property is only used when the enrollment agent is enrolling on behalf of another user. You must initialize the PKCS #7 request object before calling this property. For more information, see the following topics:<ul>
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
 

 

