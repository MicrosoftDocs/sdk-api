---
UID: NF:certenroll.IX509AttributeArchiveKey.get_EncryptedKeyBlob
title: IX509AttributeArchiveKey::get_EncryptedKeyBlob (certenroll.h)
description: Retrieves a byte array that contains the encrypted key.
helpviewer_keywords: ["EncryptedKeyBlob property [Security]","EncryptedKeyBlob property [Security]","IX509AttributeArchiveKey interface","IX509AttributeArchiveKey interface [Security]","EncryptedKeyBlob property","IX509AttributeArchiveKey.EncryptedKeyBlob","IX509AttributeArchiveKey.get_EncryptedKeyBlob","IX509AttributeArchiveKey::EncryptedKeyBlob","IX509AttributeArchiveKey::get_EncryptedKeyBlob","certenroll/IX509AttributeArchiveKey::EncryptedKeyBlob","certenroll/IX509AttributeArchiveKey::get_EncryptedKeyBlob","get_EncryptedKeyBlob","security.ix509attributearchivekey_encryptedkeyblob_property"]
old-location: security\ix509attributearchivekey_encryptedkeyblob_property.htm
tech.root: security
ms.assetid: 3230cfbf-5486-4f77-9efe-5bc542e3e096
ms.date: 12/05/2018
ms.keywords: EncryptedKeyBlob property [Security], EncryptedKeyBlob property [Security],IX509AttributeArchiveKey interface, IX509AttributeArchiveKey interface [Security],EncryptedKeyBlob property, IX509AttributeArchiveKey.EncryptedKeyBlob, IX509AttributeArchiveKey.get_EncryptedKeyBlob, IX509AttributeArchiveKey::EncryptedKeyBlob, IX509AttributeArchiveKey::get_EncryptedKeyBlob, certenroll/IX509AttributeArchiveKey::EncryptedKeyBlob, certenroll/IX509AttributeArchiveKey::get_EncryptedKeyBlob, get_EncryptedKeyBlob, security.ix509attributearchivekey_encryptedkeyblob_property
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
 - IX509AttributeArchiveKey::get_EncryptedKeyBlob
 - certenroll/IX509AttributeArchiveKey::get_EncryptedKeyBlob
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
 - IX509AttributeArchiveKey.EncryptedKeyBlob
 - IX509AttributeArchiveKey.get_EncryptedKeyBlob
---

# IX509AttributeArchiveKey::get_EncryptedKeyBlob


## -description

The <b>EncryptedKeyBlob</b> property retrieves a byte array that contains the encrypted key. The byte array is represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializedecode">InitializeDecode</a> method to initialize the <b>EncryptedKeyBlob</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionalgorithm">EncryptionAlgorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionstrength">EncryptionStrength</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>