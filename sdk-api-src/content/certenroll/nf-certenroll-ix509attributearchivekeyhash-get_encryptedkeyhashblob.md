---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
title: IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob (certenroll.h)
description: Retrieves a string that contains a hash of the encrypted private key.
helpviewer_keywords: ["EncryptedKeyHashBlob property [Security]","EncryptedKeyHashBlob property [Security]","IX509AttributeArchiveKeyHash interface","IX509AttributeArchiveKeyHash interface [Security]","EncryptedKeyHashBlob property","IX509AttributeArchiveKeyHash.EncryptedKeyHashBlob","IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob","IX509AttributeArchiveKeyHash::EncryptedKeyHashBlob","IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob","certenroll/IX509AttributeArchiveKeyHash::EncryptedKeyHashBlob","certenroll/IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob","get_EncryptedKeyHashBlob","security.ix509attributearchivekeyhash_encryptedkeyhashblob_property"]
old-location: security\ix509attributearchivekeyhash_encryptedkeyhashblob_property.htm
tech.root: security
ms.assetid: ff75aaf8-1544-465b-af0d-620ca6984249
ms.date: 12/05/2018
ms.keywords: EncryptedKeyHashBlob property [Security], EncryptedKeyHashBlob property [Security],IX509AttributeArchiveKeyHash interface, IX509AttributeArchiveKeyHash interface [Security],EncryptedKeyHashBlob property, IX509AttributeArchiveKeyHash.EncryptedKeyHashBlob, IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob, IX509AttributeArchiveKeyHash::EncryptedKeyHashBlob, IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob, certenroll/IX509AttributeArchiveKeyHash::EncryptedKeyHashBlob, certenroll/IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob, get_EncryptedKeyHashBlob, security.ix509attributearchivekeyhash_encryptedkeyhashblob_property
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
 - IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob
 - certenroll/IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob
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
 - IX509AttributeArchiveKeyHash.EncryptedKeyHashBlob
 - IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
---

# IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob


## -description

The <b>EncryptedKeyHashBlob</b> property retrieves a string that contains a <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the encrypted <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekeyhash-initializeencodefromencryptedkeyblob">InitializeEncodeFromEncryptedKeyBlob</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekeyhash-initializedecode">InitializeDecode</a> method to initialize the <b>EncryptedKeyHashBlob</b> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekeyhash">IX509AttributeArchiveKeyHash</a>