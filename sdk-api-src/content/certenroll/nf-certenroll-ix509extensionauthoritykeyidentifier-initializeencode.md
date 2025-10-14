---
UID: NF:certenroll.IX509ExtensionAuthorityKeyIdentifier.InitializeEncode
title: IX509ExtensionAuthorityKeyIdentifier::InitializeEncode (certenroll.h)
description: Initializes the extension from a byte array.
helpviewer_keywords: ["IX509ExtensionAuthorityKeyIdentifier interface [Security]","InitializeEncode method","IX509ExtensionAuthorityKeyIdentifier.InitializeEncode","IX509ExtensionAuthorityKeyIdentifier::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509ExtensionAuthorityKeyIdentifier interface","certenroll/IX509ExtensionAuthorityKeyIdentifier::InitializeEncode","security.ix509extensionauthoritykeyidentifier_initializeencode_method"]
old-location: security\ix509extensionauthoritykeyidentifier_initializeencode_method.htm
tech.root: security
ms.assetid: 450e65f9-cca0-42bd-b70b-baaf2e353812
ms.date: 12/05/2018
ms.keywords: IX509ExtensionAuthorityKeyIdentifier interface [Security],InitializeEncode method, IX509ExtensionAuthorityKeyIdentifier.InitializeEncode, IX509ExtensionAuthorityKeyIdentifier::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionAuthorityKeyIdentifier interface, certenroll/IX509ExtensionAuthorityKeyIdentifier::InitializeEncode, security.ix509extensionauthoritykeyidentifier_initializeencode_method
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
 - IX509ExtensionAuthorityKeyIdentifier::InitializeEncode
 - certenroll/IX509ExtensionAuthorityKeyIdentifier::InitializeEncode
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
 - IX509ExtensionAuthorityKeyIdentifier.InitializeEncode
---

# IX509ExtensionAuthorityKeyIdentifier::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the extension from a byte array. The byte array is represented by a Unicode-encoded string.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the <i>strKeyIdentifier</i> value.

### -param strKeyIdentifier [in]

A <b>BSTR</b> variable that contains the extension value.

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
The object is already initialized.

</td>
</tr>
</table>

## -remarks

Typically, the input value should be a SHA-1 hash of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> contained in the signing certificate. The method associates the value with the XCN_OID_AUTHORITY_KEY_IDENTIFIER2 (2.5.29.35) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and encodes it by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionauthoritykeyidentifier-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionauthoritykeyidentifier">IX509ExtensionAuthorityKeyIdentifier</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

 You can retrieve the following properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionauthoritykeyidentifier-get_authoritykeyidentifier">AuthorityKeyIdentifier</a> property retrieves the raw data.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionauthoritykeyidentifier">IX509ExtensionAuthorityKeyIdentifier</a>