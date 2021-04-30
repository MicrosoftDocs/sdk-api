---
UID: NF:certenroll.IX509CertificateRequest.get_RawData
title: IX509CertificateRequest::get_RawData (certenroll.h)
description: Retrieves a byte array that contains the signed, Distinguished Encoding Rules (DER) encoded certificate request.
helpviewer_keywords: ["IX509CertificateRequest interface [Security]","RawData property","IX509CertificateRequest.RawData","IX509CertificateRequest.get_RawData","IX509CertificateRequest::RawData","IX509CertificateRequest::get_RawData","RawData property [Security]","RawData property [Security]","IX509CertificateRequest interface","certenroll/IX509CertificateRequest::RawData","certenroll/IX509CertificateRequest::get_RawData","get_RawData","security.ix509certificaterequest_rawdata_property"]
old-location: security\ix509certificaterequest_rawdata_property.htm
tech.root: security
ms.assetid: 1830a569-03a4-4692-adbf-b627bf4370a1
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest interface [Security],RawData property, IX509CertificateRequest.RawData, IX509CertificateRequest.get_RawData, IX509CertificateRequest::RawData, IX509CertificateRequest::get_RawData, RawData property [Security], RawData property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::RawData, certenroll/IX509CertificateRequest::get_RawData, get_RawData, security.ix509certificaterequest_rawdata_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateRequest::get_RawData
 - certenroll/IX509CertificateRequest::get_RawData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest.RawData
 - IX509CertificateRequest.get_RawData
---

# IX509CertificateRequest::get_RawData


## -description

The <b>RawData</b> property retrieves a byte array that contains the signed, <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded certificate request. The byte array is represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method to encode a certificate request using DER as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array that the <b>RawData</b> property returns   as a string. The string is either a pure binary sequence, or it is Unicode encoded so that it can be displayed as text.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>