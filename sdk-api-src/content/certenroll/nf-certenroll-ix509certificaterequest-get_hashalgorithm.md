---
UID: NF:certenroll.IX509CertificateRequest.get_HashAlgorithm
title: IX509CertificateRequest::get_HashAlgorithm (certenroll.h)
description: Specifies and retrieves the object identifier (OID) of the hash algorithm used to sign the certificate request. (Get)
helpviewer_keywords: ["HashAlgorithm property [Security]","HashAlgorithm property [Security]","IX509CertificateRequest interface","IX509CertificateRequest interface [Security]","HashAlgorithm property","IX509CertificateRequest.HashAlgorithm","IX509CertificateRequest.get_HashAlgorithm","IX509CertificateRequest::HashAlgorithm","IX509CertificateRequest::get_HashAlgorithm","IX509CertificateRequest::put_HashAlgorithm","certenroll/IX509CertificateRequest::HashAlgorithm","certenroll/IX509CertificateRequest::get_HashAlgorithm","certenroll/IX509CertificateRequest::put_HashAlgorithm","get_HashAlgorithm","security.ix509certificaterequest_hashalgorithm_property"]
old-location: security\ix509certificaterequest_hashalgorithm_property.htm
tech.root: security
ms.assetid: 9f68ee54-5dea-47bb-8a90-0285d081c9b8
ms.date: 12/05/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],HashAlgorithm property, IX509CertificateRequest.HashAlgorithm, IX509CertificateRequest.get_HashAlgorithm, IX509CertificateRequest::HashAlgorithm, IX509CertificateRequest::get_HashAlgorithm, IX509CertificateRequest::put_HashAlgorithm, certenroll/IX509CertificateRequest::HashAlgorithm, certenroll/IX509CertificateRequest::get_HashAlgorithm, certenroll/IX509CertificateRequest::put_HashAlgorithm, get_HashAlgorithm, security.ix509certificaterequest_hashalgorithm_property
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
 - IX509CertificateRequest::get_HashAlgorithm
 - certenroll/IX509CertificateRequest::get_HashAlgorithm
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
 - IX509CertificateRequest.HashAlgorithm
 - IX509CertificateRequest.get_HashAlgorithm
 - IX509CertificateRequest.put_HashAlgorithm
---

# IX509CertificateRequest::get_HashAlgorithm


## -description

The <b>HashAlgorithm</b> property specifies and retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the hash algorithm used to sign the certificate request. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

If the certificate request contains nested requests and you set the <b>HashAlgorithm</b> property on the top level request, it is automatically propagated to all of the inner requests, overwriting values that may have been previously set. You can, however, set the property manually on each of the inner objects.

You must initialize the request object before calling this property. You can call this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
