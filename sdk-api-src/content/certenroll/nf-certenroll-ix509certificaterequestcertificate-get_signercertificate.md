---
UID: NF:certenroll.IX509CertificateRequestCertificate.get_SignerCertificate
title: IX509CertificateRequestCertificate::get_SignerCertificate
author: windows-sdk-content
description: Specifies or retrieves the ISignerCertificate object used to sign the certificate.
old-location: security\ix509certificaterequestcertificate_signercertificate_property.htm
tech.root: seccertenroll
ms.assetid: e3a66651-aa0d-4dbb-afb1-f2492e27fec1
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],SignerCertificate property, IX509CertificateRequestCertificate.SignerCertificate, IX509CertificateRequestCertificate.get_SignerCertificate, IX509CertificateRequestCertificate::SignerCertificate, IX509CertificateRequestCertificate::get_SignerCertificate, IX509CertificateRequestCertificate::put_SignerCertificate, SignerCertificate property [Security], SignerCertificate property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::SignerCertificate, certenroll/IX509CertificateRequestCertificate::get_SignerCertificate, certenroll/IX509CertificateRequestCertificate::put_SignerCertificate, get_SignerCertificate, security.ix509certificaterequestcertificate_signercertificate_property
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
 - IX509CertificateRequestCertificate.SignerCertificate
 - IX509CertificateRequestCertificate.get_SignerCertificate
 - IX509CertificateRequestCertificate.put_SignerCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCertificate::get_SignerCertificate


## -description


The <b>SignerCertificate</b> property specifies or retrieves the  <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object used to sign the certificate.

This property is read/write.


## -parameters


## -remarks



You can set this property if you are not creating a self-signed certificate. If you do not specify the  property value before calling  <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a>, the private key associated with the <a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a> object is used to sign the certificate, and the name of the issuer is set, by default, to the subject name.

You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377520(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377527(v=VS.85).aspx">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377531(v=VS.85).aspx">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377533(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>
 

 

