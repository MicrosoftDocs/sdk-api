---
UID: NF:certenroll.IX509CertificateRequest.put_CspInformations
title: IX509CertificateRequest::put_CspInformations (certenroll.h)
description: Specifies and retrieves a collection of cryptographic providers available for use by the request object. (Put)
helpviewer_keywords: ["CspInformations property [Security]","CspInformations property [Security]","IX509CertificateRequest interface","IX509CertificateRequest interface [Security]","CspInformations property","IX509CertificateRequest.CspInformations","IX509CertificateRequest.put_CspInformations","IX509CertificateRequest::CspInformations","IX509CertificateRequest::get_CspInformations","IX509CertificateRequest::put_CspInformations","certenroll/IX509CertificateRequest::CspInformations","certenroll/IX509CertificateRequest::get_CspInformations","certenroll/IX509CertificateRequest::put_CspInformations","put_CspInformations","security.ix509certificaterequest_cspinformations_property"]
old-location: security\ix509certificaterequest_cspinformations_property.htm
tech.root: security
ms.assetid: 7be532ab-0ab0-4c22-b274-c925fd5827d5
ms.date: 12/05/2018
ms.keywords: CspInformations property [Security], CspInformations property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],CspInformations property, IX509CertificateRequest.CspInformations, IX509CertificateRequest.put_CspInformations, IX509CertificateRequest::CspInformations, IX509CertificateRequest::get_CspInformations, IX509CertificateRequest::put_CspInformations, certenroll/IX509CertificateRequest::CspInformations, certenroll/IX509CertificateRequest::get_CspInformations, certenroll/IX509CertificateRequest::put_CspInformations, put_CspInformations, security.ix509certificaterequest_cspinformations_property
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
 - IX509CertificateRequest::put_CspInformations
 - certenroll/IX509CertificateRequest::put_CspInformations
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
 - IX509CertificateRequest.CspInformations
 - IX509CertificateRequest.get_CspInformations
 - IX509CertificateRequest.put_CspInformations
---

# IX509CertificateRequest::put_CspInformations


## -description

The <b>CspInformations</b> property specifies and retrieves a collection of cryptographic providers available for use by the request object.

This property is read/write.

## -parameters

## -remarks

If you want to specify a collection of providers, you must set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a> method. The collection that you specify must contain all providers currently installed on the computer. If you specify a subset or a superset, the behavior of this property is undefined.

If you do not specify a collection, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a> method sets the property value to a collection of all providers installed on the computer.

The <b>CspInformations</b> property exists so that the caller can avoid forcing the request object to fill the collection. This is useful when the caller is creating multiple requests in one session.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
