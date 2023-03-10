---
UID: NF:certenroll.IX509CertificateRequestCmc.get_EncryptionAlgorithm
title: IX509CertificateRequestCmc::get_EncryptionAlgorithm (certenroll.h)
description: Specifies or retrieves an object identifier (OID) of the algorithm used to encrypt the private key to be archived. (Get)
helpviewer_keywords: ["EncryptionAlgorithm property [Security]","EncryptionAlgorithm property [Security]","IX509CertificateRequestCmc interface","IX509CertificateRequestCmc interface [Security]","EncryptionAlgorithm property","IX509CertificateRequestCmc.EncryptionAlgorithm","IX509CertificateRequestCmc.get_EncryptionAlgorithm","IX509CertificateRequestCmc::EncryptionAlgorithm","IX509CertificateRequestCmc::get_EncryptionAlgorithm","IX509CertificateRequestCmc::put_EncryptionAlgorithm","certenroll/IX509CertificateRequestCmc::EncryptionAlgorithm","certenroll/IX509CertificateRequestCmc::get_EncryptionAlgorithm","certenroll/IX509CertificateRequestCmc::put_EncryptionAlgorithm","get_EncryptionAlgorithm","security.ix509certificaterequestcmc_encryptionalgorithm_property"]
old-location: security\ix509certificaterequestcmc_encryptionalgorithm_property.htm
tech.root: security
ms.assetid: c46b3373-6d9e-46d9-a36a-b73a718ddaf7
ms.date: 12/05/2018
ms.keywords: EncryptionAlgorithm property [Security], EncryptionAlgorithm property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],EncryptionAlgorithm property, IX509CertificateRequestCmc.EncryptionAlgorithm, IX509CertificateRequestCmc.get_EncryptionAlgorithm, IX509CertificateRequestCmc::EncryptionAlgorithm, IX509CertificateRequestCmc::get_EncryptionAlgorithm, IX509CertificateRequestCmc::put_EncryptionAlgorithm, certenroll/IX509CertificateRequestCmc::EncryptionAlgorithm, certenroll/IX509CertificateRequestCmc::get_EncryptionAlgorithm, certenroll/IX509CertificateRequestCmc::put_EncryptionAlgorithm, get_EncryptionAlgorithm, security.ix509certificaterequestcmc_encryptionalgorithm_property
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
 - IX509CertificateRequestCmc::get_EncryptionAlgorithm
 - certenroll/IX509CertificateRequestCmc::get_EncryptionAlgorithm
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
 - IX509CertificateRequestCmc.EncryptionAlgorithm
 - IX509CertificateRequestCmc.get_EncryptionAlgorithm
 - IX509CertificateRequestCmc.put_EncryptionAlgorithm
---

# IX509CertificateRequestCmc::get_EncryptionAlgorithm


## -description

The <b>EncryptionAlgorithm</b> property specifies or retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the algorithm used to encrypt the private key to be archived. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

When you request that a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) archive your private key, you must retrieve an exchange certificate from the CA and use the public key contained in that certificate to encrypt the private key that you are submitting for archival. The <b>EncryptionAlgorithm</b> property identifies the algorithm used to encrypt your key.

This property is related to the following properties:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_encryptedkeyhash">EncryptedKeyHash</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_encryptionstrength">EncryptionStrength</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate">KeyArchivalCertificate</a>
</li>
</ul>


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
