---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_RawDataToBeSigned
title: IX509CertificateRequestPkcs10::get_RawDataToBeSigned (certenroll.h)
description: Retrieves the unsigned certificate request created by the Encode method.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","RawDataToBeSigned property","IX509CertificateRequestPkcs10.RawDataToBeSigned","IX509CertificateRequestPkcs10.get_RawDataToBeSigned","IX509CertificateRequestPkcs10::RawDataToBeSigned","IX509CertificateRequestPkcs10::get_RawDataToBeSigned","RawDataToBeSigned property [Security]","RawDataToBeSigned property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::RawDataToBeSigned","certenroll/IX509CertificateRequestPkcs10::get_RawDataToBeSigned","get_RawDataToBeSigned","security.ix509certificaterequestpkcs10_rawdatatobesigned_property"]
old-location: security\ix509certificaterequestpkcs10_rawdatatobesigned_property.htm
tech.root: security
ms.assetid: 43e7e3e2-d94d-46b4-b76b-cd54f9d618ec
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],RawDataToBeSigned property, IX509CertificateRequestPkcs10.RawDataToBeSigned, IX509CertificateRequestPkcs10.get_RawDataToBeSigned, IX509CertificateRequestPkcs10::RawDataToBeSigned, IX509CertificateRequestPkcs10::get_RawDataToBeSigned, RawDataToBeSigned property [Security], RawDataToBeSigned property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::RawDataToBeSigned, certenroll/IX509CertificateRequestPkcs10::get_RawDataToBeSigned, get_RawDataToBeSigned, security.ix509certificaterequestpkcs10_rawdatatobesigned_property
f1_keywords:
- certenroll/IX509CertificateRequestPkcs10.RawDataToBeSigned
dev_langs:
- c++
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
- IX509CertificateRequestPkcs10.RawDataToBeSigned
- IX509CertificateRequestPkcs10.get_RawDataToBeSigned
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequestPkcs10::get_RawDataToBeSigned


## -description


The <b>RawDataToBeSigned</b> property retrieves  the unsigned certificate request created by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.   The request is contained in a byte array encoded by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read-only.


## -parameters


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method creates a DER-encoded and signed certificate request, but it also internally saves the unsigned request as a byte array. You can use the <b>RawDataToBeSigned</b> property to retrieve that binary data as an Unicode-encoded string.

 You must initialize the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object and call  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
 

 

