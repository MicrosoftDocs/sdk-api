---
UID: NF:certenroll.IX509CertificateRequestCmc.put_SenderNonce
title: IX509CertificateRequestCmc::put_SenderNonce (certenroll.h)
description: Specifies or retrieves a byte array that contains a nonce. (Put)
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","SenderNonce property","IX509CertificateRequestCmc.SenderNonce","IX509CertificateRequestCmc.put_SenderNonce","IX509CertificateRequestCmc::SenderNonce","IX509CertificateRequestCmc::get_SenderNonce","IX509CertificateRequestCmc::put_SenderNonce","SenderNonce property [Security]","SenderNonce property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::SenderNonce","certenroll/IX509CertificateRequestCmc::get_SenderNonce","certenroll/IX509CertificateRequestCmc::put_SenderNonce","put_SenderNonce","security.ix509certificaterequestcmc_sendernonce_property"]
old-location: security\ix509certificaterequestcmc_sendernonce_property.htm
tech.root: security
ms.assetid: 7f7ec18f-7b5b-445e-9033-12d86b3675f1
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SenderNonce property, IX509CertificateRequestCmc.SenderNonce, IX509CertificateRequestCmc.put_SenderNonce, IX509CertificateRequestCmc::SenderNonce, IX509CertificateRequestCmc::get_SenderNonce, IX509CertificateRequestCmc::put_SenderNonce, SenderNonce property [Security], SenderNonce property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SenderNonce, certenroll/IX509CertificateRequestCmc::get_SenderNonce, certenroll/IX509CertificateRequestCmc::put_SenderNonce, put_SenderNonce, security.ix509certificaterequestcmc_sendernonce_property
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
 - IX509CertificateRequestCmc::put_SenderNonce
 - certenroll/IX509CertificateRequestCmc::put_SenderNonce
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
 - IX509CertificateRequestCmc.SenderNonce
 - IX509CertificateRequestCmc.get_SenderNonce
 - IX509CertificateRequestCmc.put_SenderNonce
---

# IX509CertificateRequestCmc::put_SenderNonce


## -description

The <b>SenderNonce</b> property specifies or retrieves a byte array that contains a nonce. The byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read/write.

## -parameters

## -remarks

A nonce is single use, random or pseudo-random byte array that can be included in a certificate request to help ensure that the request is not a repeat of a previous message.

You can set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefrominnerrequest">InitializeFromInnerRequest</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>
