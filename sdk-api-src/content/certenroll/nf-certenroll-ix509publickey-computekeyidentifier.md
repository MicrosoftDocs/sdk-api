---
UID: NF:certenroll.IX509PublicKey.ComputeKeyIdentifier
title: IX509PublicKey::ComputeKeyIdentifier (certenroll.h)
description: Creates an identifier from a 160-bit SHA-1 hash of the public key.
helpviewer_keywords: ["ComputeKeyIdentifier","ComputeKeyIdentifier method [Security]","ComputeKeyIdentifier method [Security]","IX509PublicKey interface","IX509PublicKey interface [Security]","ComputeKeyIdentifier method","IX509PublicKey.ComputeKeyIdentifier","IX509PublicKey::ComputeKeyIdentifier","certenroll/IX509PublicKey::ComputeKeyIdentifier","security.ix509publickey_computekeyidentifier_method"]
old-location: security\ix509publickey_computekeyidentifier_method.htm
tech.root: security
ms.assetid: b2e471c7-1087-46a2-8938-5d3cea44f7f7
ms.date: 12/05/2018
ms.keywords: ComputeKeyIdentifier, ComputeKeyIdentifier method [Security], ComputeKeyIdentifier method [Security],IX509PublicKey interface, IX509PublicKey interface [Security],ComputeKeyIdentifier method, IX509PublicKey.ComputeKeyIdentifier, IX509PublicKey::ComputeKeyIdentifier, certenroll/IX509PublicKey::ComputeKeyIdentifier, security.ix509publickey_computekeyidentifier_method
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
 - IX509PublicKey::ComputeKeyIdentifier
 - certenroll/IX509PublicKey::ComputeKeyIdentifier
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
 - IX509PublicKey.ComputeKeyIdentifier
---

# IX509PublicKey::ComputeKeyIdentifier


## -description

The <b>ComputeKeyIdentifier</b> method creates an identifier from a 160-bit SHA-1 hash of the <a href="/windows/desktop/SecGloss/p-gly">public key</a>.

## -parameters

### -param Algorithm [in]

A value of the <a href="/windows/desktop/api/certenroll/ne-certenroll-keyidentifierhashalgorithm">KeyIdentifierHashAlgorithm</a> enumeration that specifies what hash algorithm to use to create the key identifier.

If this value is SKIHashDefault or SKIHashSha1, the identifier is created by hashing only the byte array that contains the key and excluding the <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) tag, length, and unused bits fields.

If this value is SKIHashCapiSha1, the identifier is created by hashing the DER-encoded byte array that contains the tag, length,  number of unused bits, and the public key.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode-encoding to be applied to the hash contained in the <i>pValue</i> parameter. The default value is XCN_CRYPT_STRING_BASE64.

### -param pValue [out]

Pointer to a <b>BSTR</b> variable that contains the key identifier.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The algorithm object identifier or the public key parameters could not be found.

</td>
</tr>
</table>

## -remarks

You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initializefromencodedpublickeyinfo">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initialize">Initialize</a> method to initialize the public key object before calling  <b>ComputeKeyIdentifier</b>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>