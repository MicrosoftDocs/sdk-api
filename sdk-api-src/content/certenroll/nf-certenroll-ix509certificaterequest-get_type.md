---
UID: NF:certenroll.IX509CertificateRequest.get_Type
title: IX509CertificateRequest::get_Type (certenroll.h)
description: Retrieves a value that specifies the type of the request object.
helpviewer_keywords: ["IX509CertificateRequest interface [Security]","Type property","IX509CertificateRequest.Type","IX509CertificateRequest.get_Type","IX509CertificateRequest::Type","IX509CertificateRequest::get_Type","Type property [Security]","Type property [Security]","IX509CertificateRequest interface","TypeCertificate","TypeCmc","TypePkcs10","TypePkcs7","certenroll/IX509CertificateRequest::Type","certenroll/IX509CertificateRequest::get_Type","get_Type","security.ix509certificaterequest_type_property"]
old-location: security\ix509certificaterequest_type_property.htm
tech.root: security
ms.assetid: 04e7e4eb-8f65-45d3-bf1d-abcb83fcf1a0
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest interface [Security],Type property, IX509CertificateRequest.Type, IX509CertificateRequest.get_Type, IX509CertificateRequest::Type, IX509CertificateRequest::get_Type, Type property [Security], Type property [Security],IX509CertificateRequest interface, TypeCertificate, TypeCmc, TypePkcs10, TypePkcs7, certenroll/IX509CertificateRequest::Type, certenroll/IX509CertificateRequest::get_Type, get_Type, security.ix509certificaterequest_type_property
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
 - IX509CertificateRequest::get_Type
 - certenroll/IX509CertificateRequest::get_Type
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
 - IX509CertificateRequest.Type
 - IX509CertificateRequest.get_Type
---

# IX509CertificateRequest::get_Type


## -description

The <b>Type</b> property retrieves a  value that specifies the type of the request object.

This property is read-only.

## -parameters

## -remarks

You can use this property with the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-getinnerrequest">GetInnerRequest</a> method to determine the type of the inner request object.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>