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
<a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377610(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377613(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377616(v=VS.85).aspx">InitializeFromInnerRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377622(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>
 

 

