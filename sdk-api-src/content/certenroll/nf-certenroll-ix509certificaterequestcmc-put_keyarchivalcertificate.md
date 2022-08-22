---
UID: NF:certenroll.IX509CertificateRequestCmc.put_KeyArchivalCertificate
title: IX509CertificateRequestCmc::put_KeyArchivalCertificate (certenroll.h)
description: Specifies or retrieves a certification authority (CA) encryption certificate. (Put)
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","KeyArchivalCertificate property","IX509CertificateRequestCmc.KeyArchivalCertificate","IX509CertificateRequestCmc.put_KeyArchivalCertificate","IX509CertificateRequestCmc::KeyArchivalCertificate","IX509CertificateRequestCmc::get_KeyArchivalCertificate","IX509CertificateRequestCmc::put_KeyArchivalCertificate","KeyArchivalCertificate property [Security]","KeyArchivalCertificate property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::KeyArchivalCertificate","certenroll/IX509CertificateRequestCmc::get_KeyArchivalCertificate","certenroll/IX509CertificateRequestCmc::put_KeyArchivalCertificate","put_KeyArchivalCertificate","security.ix509certificaterequestcmc_keyarchivalcertificate_property"]
old-location: security\ix509certificaterequestcmc_keyarchivalcertificate_property.htm
tech.root: security
ms.assetid: 93f71fd7-33bb-4352-b184-7270bca1363f
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],KeyArchivalCertificate property, IX509CertificateRequestCmc.KeyArchivalCertificate, IX509CertificateRequestCmc.put_KeyArchivalCertificate, IX509CertificateRequestCmc::KeyArchivalCertificate, IX509CertificateRequestCmc::get_KeyArchivalCertificate, IX509CertificateRequestCmc::put_KeyArchivalCertificate, KeyArchivalCertificate property [Security], KeyArchivalCertificate property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::KeyArchivalCertificate, certenroll/IX509CertificateRequestCmc::get_KeyArchivalCertificate, certenroll/IX509CertificateRequestCmc::put_KeyArchivalCertificate, put_KeyArchivalCertificate, security.ix509certificaterequestcmc_keyarchivalcertificate_property
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
 - IX509CertificateRequestCmc::put_KeyArchivalCertificate
 - certenroll/IX509CertificateRequestCmc::put_KeyArchivalCertificate
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
 - IX509CertificateRequestCmc.KeyArchivalCertificate
 - IX509CertificateRequestCmc.get_KeyArchivalCertificate
 - IX509CertificateRequestCmc.put_KeyArchivalCertificate
---

# IX509CertificateRequestCmc::put_KeyArchivalCertificate


## -description

The <b>KeyArchivalCertificate</b> property specifies or retrieves a certification authority (CA) encryption certificate. The certificate is contained in a byte array that is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

If correctly configured, a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) can archive a client's private key. Typically, the client requests an exchange certificate from the CA, validates it, and uses it as input to the <b>KeyArchivalCertificate</b> property. The CA's public key is used to encrypt the private key that is being submitted for archiving. You can use the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a> property to request key archival.

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
