---
UID: NF:certenroll.IX509EndorsementKey.AddCertificate
title: IX509EndorsementKey::AddCertificate (certenroll.h)
description: Add an endorsement key certificate to the key storage provider (KSP) that supports endorsement keys.
helpviewer_keywords: ["AddCertificate","AddCertificate method [Security]","AddCertificate method [Security]","IX509EndorsementKey interface","IX509EndorsementKey interface [Security]","AddCertificate method","IX509EndorsementKey.AddCertificate","IX509EndorsementKey::AddCertificate","certenroll/IX509EndorsementKey::AddCertificate","security.ix509endorsementkey_addcertificate"]
old-location: security\ix509endorsementkey_addcertificate.htm
tech.root: security
ms.assetid: 24621d53-c435-43e9-b709-619908f09f3b
ms.date: 12/05/2018
ms.keywords: AddCertificate, AddCertificate method [Security], AddCertificate method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],AddCertificate method, IX509EndorsementKey.AddCertificate, IX509EndorsementKey::AddCertificate, certenroll/IX509EndorsementKey::AddCertificate, security.ix509endorsementkey_addcertificate
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509EndorsementKey::AddCertificate
 - certenroll/IX509EndorsementKey::AddCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509EndorsementKey.AddCertificate
---

# IX509EndorsementKey::AddCertificate


## -description

Add an endorsement key certificate to the key storage provider (KSP) that supports endorsement keys. You can only call the <b>AddCertificate</b> method after the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a> method has been successfully called.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the certificate. The default value is XCN_CRYPT_STRING_BASE64.

### -param strCertificate [in]

The certificate to add to the store. The public key from this certificate must match the public key of the endorsement key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only non-manufacturer certificates can be added to the key storage provider.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509endorsementkey">IX509EndorsementKey</a>