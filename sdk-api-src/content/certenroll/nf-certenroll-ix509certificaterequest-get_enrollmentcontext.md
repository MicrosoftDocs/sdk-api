---
UID: NF:certenroll.IX509CertificateRequest.get_EnrollmentContext
title: IX509CertificateRequest::get_EnrollmentContext (certenroll.h)
description: Retrieves a value that specifies whether the certificate is intended for a computer or a user.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","EnrollmentContext property [Security]","EnrollmentContext property [Security]","IX509CertificateRequest interface","IX509CertificateRequest interface [Security]","EnrollmentContext property","IX509CertificateRequest.EnrollmentContext","IX509CertificateRequest.get_EnrollmentContext","IX509CertificateRequest::EnrollmentContext","IX509CertificateRequest::get_EnrollmentContext","certenroll/IX509CertificateRequest::EnrollmentContext","certenroll/IX509CertificateRequest::get_EnrollmentContext","get_EnrollmentContext","security.ix509certificaterequest_enrollmentcontext_property"]
old-location: security\ix509certificaterequest_enrollmentcontext_property.htm
tech.root: security
ms.assetid: ea0fa54d-0de6-4578-b93a-1e399101006b
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, EnrollmentContext property [Security], EnrollmentContext property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],EnrollmentContext property, IX509CertificateRequest.EnrollmentContext, IX509CertificateRequest.get_EnrollmentContext, IX509CertificateRequest::EnrollmentContext, IX509CertificateRequest::get_EnrollmentContext, certenroll/IX509CertificateRequest::EnrollmentContext, certenroll/IX509CertificateRequest::get_EnrollmentContext, get_EnrollmentContext, security.ix509certificaterequest_enrollmentcontext_property
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
 - IX509CertificateRequest::get_EnrollmentContext
 - certenroll/IX509CertificateRequest::get_EnrollmentContext
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
 - IX509CertificateRequest.EnrollmentContext
 - IX509CertificateRequest.get_EnrollmentContext
---

# IX509CertificateRequest::get_EnrollmentContext


## -description

The <b>EnrollmentContext</b> property retrieves a value that specifies whether the certificate is intended for a computer or a user.

This property is read-only.

## -parameters

## -remarks

For a PKCS #7 or CMC request, the property value is retrieved from the inner request object.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>