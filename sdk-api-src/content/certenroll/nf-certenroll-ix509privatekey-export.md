---
UID: NF:certenroll.IX509PrivateKey.Export
title: IX509PrivateKey::Export (certenroll.h)
description: Copies the private key to a byte array.
helpviewer_keywords: ["BCRYPT_PRIVATE_KEY_BLOB","BCRYPT_PUBLIC_KEY_BLOB","Export","Export method [Security]","Export method [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","Export method","IX509PrivateKey.Export","IX509PrivateKey::Export","certenroll/IX509PrivateKey::Export","security.ix509privatekey_export_method"]
old-location: security\ix509privatekey_export_method.htm
tech.root: security
ms.assetid: 86316966-11d5-42d6-8690-eddfe86f8150
ms.date: 12/05/2018
ms.keywords: BCRYPT_PRIVATE_KEY_BLOB, BCRYPT_PUBLIC_KEY_BLOB, Export, Export method [Security], Export method [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Export method, IX509PrivateKey.Export, IX509PrivateKey::Export, certenroll/IX509PrivateKey::Export, security.ix509privatekey_export_method
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
 - IX509PrivateKey::Export
 - certenroll/IX509PrivateKey::Export
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
 - IX509PrivateKey.Export
---

# IX509PrivateKey::Export


## -description

The <b>Export</b> method copies the private key to a byte array. The byte array is represented by a Unicode-encoded string.

## -parameters

### -param strExportType [in]

A <b>BSTR</b> value that specifies how the private key is exported. 

If the key was created by using a CNG KSP (Key Storage Provider), you can specify one of the values allowed by the <i>pszBlobType</i> parameter in the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptexportkey">NCryptExportKey</a> function.

If the key was created by using a CryptoAPI CSP (Cryptographic Service Provider), you can specify one of the following values from the Bcrypt.h header file included with Wincrypt.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PUBLIC_KEY_BLOB"></a><a id="bcrypt_public_key_blob"></a><dl>
<dt><b>BCRYPT_PUBLIC_KEY_BLOB</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Exports only the public portion of the private key.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PRIVATE_KEY_BLOB"></a><a id="bcrypt_private_key_blob"></a><dl>
<dt><b>BCRYPT_PRIVATE_KEY_BLOB</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Exports the entire private key.

</td>
</tr>
</table>

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding to be applied to the string contained in the <i>pstrEncodedKey</i> parameter. The default value is XCN_CRYPT_STRING_BASE64.

### -param pstrEncodedKey [out]

Pointer to a <b>BSTR</b> variable that contains the private key.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CALL_NOT_IMPLEMENTED)</b></dt>
</dl>
</td>
<td width="60%">
The key was created by a CryptoAPI CSP and you specified a value other than BCRYPT_PRIVATE_KEY_BLOB or BCRYPT_PUBLIC_KEY_BLOB for the <i>strExportType</i> parameter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>