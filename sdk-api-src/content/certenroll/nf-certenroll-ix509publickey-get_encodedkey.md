---
UID: NF:certenroll.IX509PublicKey.get_EncodedKey
title: IX509PublicKey::get_EncodedKey (certenroll.h)
description: Retrieves a byte array that contains the public key.
helpviewer_keywords: ["EncodedKey property [Security]","EncodedKey property [Security]","IX509PublicKey interface","IX509PublicKey interface [Security]","EncodedKey property","IX509PublicKey.EncodedKey","IX509PublicKey.get_EncodedKey","IX509PublicKey::EncodedKey","IX509PublicKey::get_EncodedKey","certenroll/IX509PublicKey::EncodedKey","certenroll/IX509PublicKey::get_EncodedKey","get_EncodedKey","security.ix509publickey_encodedkey_property"]
old-location: security\ix509publickey_encodedkey_property.htm
tech.root: security
ms.assetid: 3573f4b6-ecfd-4540-bc43-c88943992fe2
ms.date: 12/05/2018
ms.keywords: EncodedKey property [Security], EncodedKey property [Security],IX509PublicKey interface, IX509PublicKey interface [Security],EncodedKey property, IX509PublicKey.EncodedKey, IX509PublicKey.get_EncodedKey, IX509PublicKey::EncodedKey, IX509PublicKey::get_EncodedKey, certenroll/IX509PublicKey::EncodedKey, certenroll/IX509PublicKey::get_EncodedKey, get_EncodedKey, security.ix509publickey_encodedkey_property
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
 - IX509PublicKey::get_EncodedKey
 - certenroll/IX509PublicKey::get_EncodedKey
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
 - IX509PublicKey.EncodedKey
 - IX509PublicKey.get_EncodedKey
---

# IX509PublicKey::get_EncodedKey


## -description

The <b>EncodedKey</b> property retrieves a byte array that contains the public key.  The byte array is represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initializefromencodedpublickeyinfo">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initialize">Initialize</a> method to initialize the public key object before calling this property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>