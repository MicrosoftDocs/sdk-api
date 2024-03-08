---
UID: NF:certenroll.IX509CertificateRequestCmc.put_ArchivePrivateKey
title: IX509CertificateRequestCmc::put_ArchivePrivateKey (certenroll.h)
description: Specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA). (Put)
helpviewer_keywords: ["ArchivePrivateKey property [Security]","ArchivePrivateKey property [Security]","IX509CertificateRequestCmc interface","IX509CertificateRequestCmc interface [Security]","ArchivePrivateKey property","IX509CertificateRequestCmc.ArchivePrivateKey","IX509CertificateRequestCmc.put_ArchivePrivateKey","IX509CertificateRequestCmc::ArchivePrivateKey","IX509CertificateRequestCmc::get_ArchivePrivateKey","IX509CertificateRequestCmc::put_ArchivePrivateKey","certenroll/IX509CertificateRequestCmc::ArchivePrivateKey","certenroll/IX509CertificateRequestCmc::get_ArchivePrivateKey","certenroll/IX509CertificateRequestCmc::put_ArchivePrivateKey","put_ArchivePrivateKey","security.ix509certificaterequestcmc_archiveprivatekey_property"]
old-location: security\ix509certificaterequestcmc_archiveprivatekey_property.htm
tech.root: security
ms.assetid: 6d17222e-3657-4911-a8e7-d90214284441
ms.date: 12/05/2018
ms.keywords: ArchivePrivateKey property [Security], ArchivePrivateKey property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],ArchivePrivateKey property, IX509CertificateRequestCmc.ArchivePrivateKey, IX509CertificateRequestCmc.put_ArchivePrivateKey, IX509CertificateRequestCmc::ArchivePrivateKey, IX509CertificateRequestCmc::get_ArchivePrivateKey, IX509CertificateRequestCmc::put_ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::get_ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::put_ArchivePrivateKey, put_ArchivePrivateKey, security.ix509certificaterequestcmc_archiveprivatekey_property
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
 - IX509CertificateRequestCmc::put_ArchivePrivateKey
 - certenroll/IX509CertificateRequestCmc::put_ArchivePrivateKey
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
 - IX509CertificateRequestCmc.ArchivePrivateKey
 - IX509CertificateRequestCmc.get_ArchivePrivateKey
 - IX509CertificateRequestCmc.put_ArchivePrivateKey
---

# IX509CertificateRequestCmc::put_ArchivePrivateKey


## -description

The <b>ArchivePrivateKey</b> property specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA).

This property is read/write.

## -parameters

## -remarks

To request that a CA archive your private key, you must also set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate">KeyArchivalCertificate</a> property with the CA encryption (key exchange) certificate.

You can set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method, but you must initialize the CMC request object before setting the property value. For more information, see the following topics:<ul>
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
