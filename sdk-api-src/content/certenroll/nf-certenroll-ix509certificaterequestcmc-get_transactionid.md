---
UID: NF:certenroll.IX509CertificateRequestCmc.get_TransactionId
title: IX509CertificateRequestCmc::get_TransactionId (certenroll.h)
description: Specifies or retrieves a transaction identifier that can be used to track a certificate request or response. (Get)
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","TransactionId property","IX509CertificateRequestCmc.TransactionId","IX509CertificateRequestCmc.get_TransactionId","IX509CertificateRequestCmc::TransactionId","IX509CertificateRequestCmc::get_TransactionId","IX509CertificateRequestCmc::put_TransactionId","TransactionId property [Security]","TransactionId property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::TransactionId","certenroll/IX509CertificateRequestCmc::get_TransactionId","certenroll/IX509CertificateRequestCmc::put_TransactionId","get_TransactionId","security.ix509certificaterequestcmc_transactionid_property"]
old-location: security\ix509certificaterequestcmc_transactionid_property.htm
tech.root: security
ms.assetid: 0d47e4b6-47bb-4ec4-8248-f4c859e9b9da
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],TransactionId property, IX509CertificateRequestCmc.TransactionId, IX509CertificateRequestCmc.get_TransactionId, IX509CertificateRequestCmc::TransactionId, IX509CertificateRequestCmc::get_TransactionId, IX509CertificateRequestCmc::put_TransactionId, TransactionId property [Security], TransactionId property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::TransactionId, certenroll/IX509CertificateRequestCmc::get_TransactionId, certenroll/IX509CertificateRequestCmc::put_TransactionId, get_TransactionId, security.ix509certificaterequestcmc_transactionid_property
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
 - IX509CertificateRequestCmc::get_TransactionId
 - certenroll/IX509CertificateRequestCmc::get_TransactionId
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
 - IX509CertificateRequestCmc.TransactionId
 - IX509CertificateRequestCmc.get_TransactionId
 - IX509CertificateRequestCmc.put_TransactionId
---

# IX509CertificateRequestCmc::get_TransactionId


## -description

The <b>TransactionId</b> property specifies or retrieves a transaction identifier that can be used to track a certificate request or response.

This property is read/write.

## -parameters

## -remarks

 A round trip certificate request and response transaction can be tracked using an identifier.  The client generates a transaction ID and
   retains it until the certificate or registration authority responds with a message that
   completes the transaction.  The  response includes the identifier.

You must set this property, if at all,  before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
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
