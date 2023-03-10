---
UID: NF:certenroll.IX509CertificateRequest.put_SuppressDefaults
title: IX509CertificateRequest::put_SuppressDefaults (certenroll.h)
description: Specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request. (Put)
helpviewer_keywords: ["IX509CertificateRequest interface [Security]","SuppressDefaults property","IX509CertificateRequest.SuppressDefaults","IX509CertificateRequest.put_SuppressDefaults","IX509CertificateRequest::SuppressDefaults","IX509CertificateRequest::get_SuppressDefaults","IX509CertificateRequest::put_SuppressDefaults","SuppressDefaults property [Security]","SuppressDefaults property [Security]","IX509CertificateRequest interface","certenroll/IX509CertificateRequest::SuppressDefaults","certenroll/IX509CertificateRequest::get_SuppressDefaults","certenroll/IX509CertificateRequest::put_SuppressDefaults","put_SuppressDefaults","security.ix509certificaterequest_suppressdefaults_property"]
old-location: security\ix509certificaterequest_suppressdefaults_property.htm
tech.root: security
ms.assetid: 3a7847b6-52b4-4058-8113-cbc3b9101a5b
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest interface [Security],SuppressDefaults property, IX509CertificateRequest.SuppressDefaults, IX509CertificateRequest.put_SuppressDefaults, IX509CertificateRequest::SuppressDefaults, IX509CertificateRequest::get_SuppressDefaults, IX509CertificateRequest::put_SuppressDefaults, SuppressDefaults property [Security], SuppressDefaults property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::SuppressDefaults, certenroll/IX509CertificateRequest::get_SuppressDefaults, certenroll/IX509CertificateRequest::put_SuppressDefaults, put_SuppressDefaults, security.ix509certificaterequest_suppressdefaults_property
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
 - IX509CertificateRequest::put_SuppressDefaults
 - certenroll/IX509CertificateRequest::put_SuppressDefaults
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
 - IX509CertificateRequest.SuppressDefaults
 - IX509CertificateRequest.get_SuppressDefaults
 - IX509CertificateRequest.put_SuppressDefaults
---

# IX509CertificateRequest::put_SuppressDefaults


## -description

The <b>SuppressDefaults</b> property specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request. The defaults are represented by their <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs).

This property is read/write.

## -parameters

## -remarks

You must initialize the request object before calling this property. Set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method to suppress inclusion and encoding of default extensions and attributes in the certificate request.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
