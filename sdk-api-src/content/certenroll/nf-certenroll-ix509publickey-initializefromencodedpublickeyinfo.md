---
UID: NF:certenroll.IX509PublicKey.InitializeFromEncodedPublicKeyInfo
title: IX509PublicKey::InitializeFromEncodedPublicKeyInfo (certenroll.h)
description: Initializes the object from a byte array that contains a public key.
helpviewer_keywords: ["IX509PublicKey interface [Security]","InitializeFromEncodedPublicKeyInfo method","IX509PublicKey.InitializeFromEncodedPublicKeyInfo","IX509PublicKey::InitializeFromEncodedPublicKeyInfo","InitializeFromEncodedPublicKeyInfo","InitializeFromEncodedPublicKeyInfo method [Security]","InitializeFromEncodedPublicKeyInfo method [Security]","IX509PublicKey interface","certenroll/IX509PublicKey::InitializeFromEncodedPublicKeyInfo","security.ix509publickey_initializefromencodedpublickeyinfo_method"]
old-location: security\ix509publickey_initializefromencodedpublickeyinfo_method.htm
tech.root: security
ms.assetid: 3e92d934-1ab7-4f09-a579-0dde4ef44c7f
ms.date: 12/05/2018
ms.keywords: IX509PublicKey interface [Security],InitializeFromEncodedPublicKeyInfo method, IX509PublicKey.InitializeFromEncodedPublicKeyInfo, IX509PublicKey::InitializeFromEncodedPublicKeyInfo, InitializeFromEncodedPublicKeyInfo, InitializeFromEncodedPublicKeyInfo method [Security], InitializeFromEncodedPublicKeyInfo method [Security],IX509PublicKey interface, certenroll/IX509PublicKey::InitializeFromEncodedPublicKeyInfo, security.ix509publickey_initializefromencodedpublickeyinfo_method
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
 - IX509PublicKey::InitializeFromEncodedPublicKeyInfo
 - certenroll/IX509PublicKey::InitializeFromEncodedPublicKeyInfo
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
 - IX509PublicKey.InitializeFromEncodedPublicKeyInfo
---

# IX509PublicKey::InitializeFromEncodedPublicKeyInfo


## -description

The <b>InitializeFromEncodedPublicKeyInfo</b> method initializes the object from a byte array that contains a public key. The byte array is represented by a Unicode-encoded string.

## -parameters

### -param strEncodedPublicKeyInfo [in]

A <b>BSTR</b> variable that contains the key.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the key contained in the <i>strEncodedPublicKeyInfo</i> parameter. The default value is XCN_CRYPT_STRING_BASE64.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object has already been initialized.

</td>
</tr>
</table>

## -remarks

The <b>InitializeFromEncodedPublicKeyInfo</b> method initializes the following property values from an existing public key:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-get_algorithm">Algorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-get_encodedkey">EncodedKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-get_encodedparameters">EncodedParameters</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-get_length">Length</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>