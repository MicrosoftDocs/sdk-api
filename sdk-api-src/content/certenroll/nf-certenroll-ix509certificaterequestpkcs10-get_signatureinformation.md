---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_SignatureInformation
title: IX509CertificateRequestPkcs10::get_SignatureInformation
author: windows-sdk-content
description: Retrieves the IX509SignatureInformation object that contains information about the certificate request signature.
old-location: security\ix509certificaterequestpkcs10_signatureinformation_property.htm
old-project: seccertenroll
ms.assetid: d90a8b82-a4d7-4d31-bcd0-293572a2bdd2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],SignatureInformation property, IX509CertificateRequestPkcs10.SignatureInformation, IX509CertificateRequestPkcs10.get_SignatureInformation, IX509CertificateRequestPkcs10::SignatureInformation, IX509CertificateRequestPkcs10::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::SignatureInformation, certenroll/IX509CertificateRequestPkcs10::get_SignatureInformation, get_SignatureInformation, security.ix509certificaterequestpkcs10_signatureinformation_property
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
 - IX509CertificateRequestPkcs10.SignatureInformation
 - IX509CertificateRequestPkcs10.get_SignatureInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_SignatureInformation


## -description


The <b>SignatureInformation</b> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object that contains information about the certificate request signature. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object contains information about the hash, public key and signature algorithms used to sign the certificate request. If no <b>IX509SignatureInformation</b> object has been associated with the request, this property attempts to create one and use the private key to set the <a href="https://msdn.microsoft.com/en-us/library/Aa379059(v=VS.85).aspx">PublicKeyAlgorithm</a> property.

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
 

 

