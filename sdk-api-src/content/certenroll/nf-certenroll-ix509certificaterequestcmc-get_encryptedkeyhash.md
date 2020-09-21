---
UID: NF:certenroll.IX509CertificateRequestCmc.get_EncryptedKeyHash
title: IX509CertificateRequestCmc::get_EncryptedKeyHash (certenroll.h)
description: Retrieves a hash of the private key to be archived.
helpviewer_keywords: ["EncryptedKeyHash property [Security]","EncryptedKeyHash property [Security]","IX509CertificateRequestCmc interface","IX509CertificateRequestCmc interface [Security]","EncryptedKeyHash property","IX509CertificateRequestCmc.EncryptedKeyHash","IX509CertificateRequestCmc.get_EncryptedKeyHash","IX509CertificateRequestCmc::EncryptedKeyHash","IX509CertificateRequestCmc::get_EncryptedKeyHash","certenroll/IX509CertificateRequestCmc::EncryptedKeyHash","certenroll/IX509CertificateRequestCmc::get_EncryptedKeyHash","get_EncryptedKeyHash","security.ix509certificaterequestcmc_encryptedkeyhash_property"]
old-location: security\ix509certificaterequestcmc_encryptedkeyhash_property.htm
tech.root: security
ms.assetid: 63aba8aa-bee7-46b6-a821-4e4d440356ac
ms.date: 12/05/2018
ms.keywords: EncryptedKeyHash property [Security], EncryptedKeyHash property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],EncryptedKeyHash property, IX509CertificateRequestCmc.EncryptedKeyHash, IX509CertificateRequestCmc.get_EncryptedKeyHash, IX509CertificateRequestCmc::EncryptedKeyHash, IX509CertificateRequestCmc::get_EncryptedKeyHash, certenroll/IX509CertificateRequestCmc::EncryptedKeyHash, certenroll/IX509CertificateRequestCmc::get_EncryptedKeyHash, get_EncryptedKeyHash, security.ix509certificaterequestcmc_encryptedkeyhash_property
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
 - IX509CertificateRequestCmc::get_EncryptedKeyHash
 - certenroll/IX509CertificateRequestCmc::get_EncryptedKeyHash
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
 - IX509CertificateRequestCmc.EncryptedKeyHash
 - IX509CertificateRequestCmc.get_EncryptedKeyHash
---

# IX509CertificateRequestCmc::get_EncryptedKeyHash


## -description

The <b>EncryptedKeyHash</b> property retrieves a hash of the private key to be archived. The hash is contained in an encoded byte array.

This property is read-only.

## -parameters

## -remarks

For more information about archiving private keys, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate">KeyArchivalCertificate</a> properties.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>