---
UID: NF:certenroll.IX509AttributeArchiveKey.get_EncryptionAlgorithm
title: IX509AttributeArchiveKey::get_EncryptionAlgorithm (certenroll.h)
description: Retrieves the object identifier (OID) of the symmetric encryption algorithm used to encrypt the private key.
helpviewer_keywords: ["EncryptionAlgorithm property [Security]","EncryptionAlgorithm property [Security]","IX509AttributeArchiveKey interface","IX509AttributeArchiveKey interface [Security]","EncryptionAlgorithm property","IX509AttributeArchiveKey.EncryptionAlgorithm","IX509AttributeArchiveKey.get_EncryptionAlgorithm","IX509AttributeArchiveKey::EncryptionAlgorithm","IX509AttributeArchiveKey::get_EncryptionAlgorithm","certenroll/IX509AttributeArchiveKey::EncryptionAlgorithm","certenroll/IX509AttributeArchiveKey::get_EncryptionAlgorithm","get_EncryptionAlgorithm","security.ix509attributearchivekey_encryptionalgorithm_property"]
old-location: security\ix509attributearchivekey_encryptionalgorithm_property.htm
tech.root: security
ms.assetid: 7aef6c1e-c3f1-4124-b397-bf13ca610135
ms.date: 12/05/2018
ms.keywords: EncryptionAlgorithm property [Security], EncryptionAlgorithm property [Security],IX509AttributeArchiveKey interface, IX509AttributeArchiveKey interface [Security],EncryptionAlgorithm property, IX509AttributeArchiveKey.EncryptionAlgorithm, IX509AttributeArchiveKey.get_EncryptionAlgorithm, IX509AttributeArchiveKey::EncryptionAlgorithm, IX509AttributeArchiveKey::get_EncryptionAlgorithm, certenroll/IX509AttributeArchiveKey::EncryptionAlgorithm, certenroll/IX509AttributeArchiveKey::get_EncryptionAlgorithm, get_EncryptionAlgorithm, security.ix509attributearchivekey_encryptionalgorithm_property
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
 - IX509AttributeArchiveKey::get_EncryptionAlgorithm
 - certenroll/IX509AttributeArchiveKey::get_EncryptionAlgorithm
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
 - IX509AttributeArchiveKey.EncryptionAlgorithm
 - IX509AttributeArchiveKey.get_EncryptionAlgorithm
---

# IX509AttributeArchiveKey::get_EncryptionAlgorithm


## -description

The <b>EncryptionAlgorithm</b> property retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the symmetric encryption algorithm used to encrypt the <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializedecode">InitializeDecode</a> method to initialize the <b>EncryptionAlgorithm</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptedkeyblob">EncryptedKeyBlob</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionstrength">EncryptionStrength</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>