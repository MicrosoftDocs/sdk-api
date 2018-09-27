---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_OldCertificate
title: IX509CertificateRequestPkcs10::get_OldCertificate
author: windows-sdk-content
description: Retrieves the certificate passed to the InitializeFromCertificate method.
old-location: security\ix509certificaterequestpkcs10_oldcertificate_property.htm
tech.root: seccertenroll
ms.assetid: 8bb15b5c-e642-477d-bcec-772748e336ef
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],OldCertificate property, IX509CertificateRequestPkcs10.OldCertificate, IX509CertificateRequestPkcs10.get_OldCertificate, IX509CertificateRequestPkcs10::OldCertificate, IX509CertificateRequestPkcs10::get_OldCertificate, OldCertificate property [Security], OldCertificate property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::OldCertificate, certenroll/IX509CertificateRequestPkcs10::get_OldCertificate, get_OldCertificate, security.ix509certificaterequestpkcs10_oldcertificate_property
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
 - IX509CertificateRequestPkcs10.OldCertificate
 - IX509CertificateRequestPkcs10.get_OldCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_OldCertificate


## -description


The <b>OldCertificate</b> property retrieves the certificate passed to the <a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a> method.  The certificate is contained in a byte array encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read-only.


## -parameters


## -remarks



 You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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




<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

