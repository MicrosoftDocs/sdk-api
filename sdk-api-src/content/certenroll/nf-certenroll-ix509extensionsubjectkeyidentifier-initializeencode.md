---
UID: NF:certenroll.IX509ExtensionSubjectKeyIdentifier.InitializeEncode
title: IX509ExtensionSubjectKeyIdentifier::InitializeEncode (certenroll.h)
description: Initializes the extension from a byte array that contains the key identifier.
helpviewer_keywords: ["IX509ExtensionSubjectKeyIdentifier interface [Security]","InitializeEncode method","IX509ExtensionSubjectKeyIdentifier.InitializeEncode","IX509ExtensionSubjectKeyIdentifier::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509ExtensionSubjectKeyIdentifier interface","certenroll/IX509ExtensionSubjectKeyIdentifier::InitializeEncode","security.ix509extensionsubjectkeyidentifier_initializeencode_method"]
old-location: security\ix509extensionsubjectkeyidentifier_initializeencode_method.htm
tech.root: security
ms.assetid: 0faf3567-3908-473e-9f5c-392991ea668c
ms.date: 12/05/2018
ms.keywords: IX509ExtensionSubjectKeyIdentifier interface [Security],InitializeEncode method, IX509ExtensionSubjectKeyIdentifier.InitializeEncode, IX509ExtensionSubjectKeyIdentifier::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionSubjectKeyIdentifier interface, certenroll/IX509ExtensionSubjectKeyIdentifier::InitializeEncode, security.ix509extensionsubjectkeyidentifier_initializeencode_method
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
 - IX509ExtensionSubjectKeyIdentifier::InitializeEncode
 - certenroll/IX509ExtensionSubjectKeyIdentifier::InitializeEncode
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
 - IX509ExtensionSubjectKeyIdentifier.InitializeEncode
---

# IX509ExtensionSubjectKeyIdentifier::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the extension from a byte array that contains the key identifier. The byte array is represented by a Unicode-encoded string.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the <i>strKeyIdentifier</i> parameter.

### -param strKeyIdentifier [in]

A <b>BSTR</b> variable that contains the key identifier.

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

Typically, the input value should be a SHA-1 hash of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> contained in the certification authority signing certificate. The method associates the value with the XCN_OID_SUBJECT_KEY_IDENTIFIER (2.5.29.14) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and encodes it by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionauthoritykeyidentifier-get_authoritykeyidentifier">AuthorityKeyIdentifier</a> property retrieves the raw data.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a>