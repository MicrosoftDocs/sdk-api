---
UID: NF:certenroll.IX509CertificateRequest.get_RenewalCertificate
title: IX509CertificateRequest::get_RenewalCertificate (certenroll.h)
description: Specifies or retrieves a byte array that contains the Distinguished Encoding Rules (DER) encoded certificate that is being renewed.helpviewer_keywords: ["IX509CertificateRequest interface [Security]","RenewalCertificate property","IX509CertificateRequest.RenewalCertificate","IX509CertificateRequest.get_RenewalCertificate","IX509CertificateRequest::RenewalCertificate","IX509CertificateRequest::get_RenewalCertificate","IX509CertificateRequest::put_RenewalCertificate","RenewalCertificate property [Security]","RenewalCertificate property [Security]","IX509CertificateRequest interface","certenroll/IX509CertificateRequest::RenewalCertificate","certenroll/IX509CertificateRequest::get_RenewalCertificate","certenroll/IX509CertificateRequest::put_RenewalCertificate","get_RenewalCertificate","security.ix509certificaterequest_renewalcertificate_property"]
old-location: security\ix509certificaterequest_renewalcertificate_property.htm
tech.root: seccertenroll
ms.assetid: ab046b65-a059-4b48-a6cd-7e2f0b18bc65
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest interface [Security],RenewalCertificate property, IX509CertificateRequest.RenewalCertificate, IX509CertificateRequest.get_RenewalCertificate, IX509CertificateRequest::RenewalCertificate, IX509CertificateRequest::get_RenewalCertificate, IX509CertificateRequest::put_RenewalCertificate, RenewalCertificate property [Security], RenewalCertificate property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::RenewalCertificate, certenroll/IX509CertificateRequest::get_RenewalCertificate, certenroll/IX509CertificateRequest::put_RenewalCertificate, get_RenewalCertificate, security.ix509certificaterequest_renewalcertificate_property
f1_keywords:
- certenroll/IX509CertificateRequest.RenewalCertificate
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
- IX509CertificateRequest.RenewalCertificate
- IX509CertificateRequest.get_RenewalCertificate
- IX509CertificateRequest.put_RenewalCertificate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequest::get_RenewalCertificate


## -description


The <b>RenewalCertificate</b> property specifies or retrieves a byte array that contains the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded certificate that is being renewed.  The DER-encoded byte array is represented by a Unicode-encoded string.

This property is read/write.


## -parameters


## -remarks



The certificate is encoded by using DER as defined by the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array. The byte array is returned in a  string that is either a pure binary sequence or is Unicode encoded so that it can be displayed as text.

You must initialize the request object before calling this property. You can call this property before calling the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
 

 

