---
UID: NF:certenroll.IX509CertificateRequestCmc.get_EncryptionStrength
title: IX509CertificateRequestCmc::get_EncryptionStrength (certenroll.h)
description: Specifies or retrieves the relative encryption level applied to the private key to be archived. (Get)
helpviewer_keywords: ["EncryptionStrength property [Security]","EncryptionStrength property [Security]","IX509CertificateRequestCmc interface","IX509CertificateRequestCmc interface [Security]","EncryptionStrength property","IX509CertificateRequestCmc.EncryptionStrength","IX509CertificateRequestCmc.get_EncryptionStrength","IX509CertificateRequestCmc::EncryptionStrength","IX509CertificateRequestCmc::get_EncryptionStrength","IX509CertificateRequestCmc::put_EncryptionStrength","certenroll/IX509CertificateRequestCmc::EncryptionStrength","certenroll/IX509CertificateRequestCmc::get_EncryptionStrength","certenroll/IX509CertificateRequestCmc::put_EncryptionStrength","get_EncryptionStrength","security.ix509certificaterequestcmc_encryptionstrength_property"]
old-location: security\ix509certificaterequestcmc_encryptionstrength_property.htm
tech.root: security
ms.assetid: 9cade9f0-d614-4838-bf42-0a19b4ce53d5
ms.date: 12/05/2018
ms.keywords: EncryptionStrength property [Security], EncryptionStrength property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],EncryptionStrength property, IX509CertificateRequestCmc.EncryptionStrength, IX509CertificateRequestCmc.get_EncryptionStrength, IX509CertificateRequestCmc::EncryptionStrength, IX509CertificateRequestCmc::get_EncryptionStrength, IX509CertificateRequestCmc::put_EncryptionStrength, certenroll/IX509CertificateRequestCmc::EncryptionStrength, certenroll/IX509CertificateRequestCmc::get_EncryptionStrength, certenroll/IX509CertificateRequestCmc::put_EncryptionStrength, get_EncryptionStrength, security.ix509certificaterequestcmc_encryptionstrength_property
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
 - IX509CertificateRequestCmc::get_EncryptionStrength
 - certenroll/IX509CertificateRequestCmc::get_EncryptionStrength
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
 - IX509CertificateRequestCmc.EncryptionStrength
 - IX509CertificateRequestCmc.get_EncryptionStrength
 - IX509CertificateRequestCmc.put_EncryptionStrength
---

# IX509CertificateRequestCmc::get_EncryptionStrength


## -description

The <b>EncryptionStrength</b> property specifies or retrieves the relative encryption level applied to the private key to be archived.

This property is read/write.

## -parameters

## -remarks

This property is related to the following properties:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_encryptedkeyhash">EncryptedKeyHash</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_encryptionalgorithm">EncryptionAlgorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate">KeyArchivalCertificate</a>
</li>
</ul>


The encryption strength is often implied by the encryption algorithm. If the algorithm does not support multiple strengths, you should not set the <b>EncryptionStrength</b> property.

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
