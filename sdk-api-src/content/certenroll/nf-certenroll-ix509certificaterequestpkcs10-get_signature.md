---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_Signature
title: IX509CertificateRequestPkcs10::get_Signature
author: windows-sdk-content
description: Retrieves the request signature created by the Encode method.
old-location: security\ix509certificaterequestpkcs10_signature_property.htm
tech.root: SecCertEnroll
ms.assetid: ee6ad3c7-2d31-4a12-ad37-ee6e1071b665
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],Signature property, IX509CertificateRequestPkcs10.Signature, IX509CertificateRequestPkcs10.get_Signature, IX509CertificateRequestPkcs10::Signature, IX509CertificateRequestPkcs10::get_Signature, Signature property [Security], Signature property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::Signature, certenroll/IX509CertificateRequestPkcs10::get_Signature, get_Signature, security.ix509certificaterequestpkcs10_signature_property
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
 - IX509CertificateRequestPkcs10.Signature
 - IX509CertificateRequestPkcs10.get_Signature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509CertificateRequestPkcs10.get_Signature
: 
---

# IX509CertificateRequestPkcs10::get_Signature


## -description


The <b>Signature</b> property retrieves the request signature created by the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method. The signature is contained in a byte array encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method creates a DER-encoded and signed certificate request which it saves internally as a byte array. You can use the <b>Signature</b> property to retrieve a byte array that contains the signature.

 You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object and call  <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> before calling this property. For more information, see any of the following methods:<ul>
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
 

 

