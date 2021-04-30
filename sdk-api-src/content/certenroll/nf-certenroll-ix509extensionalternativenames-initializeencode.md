---
UID: NF:certenroll.IX509ExtensionAlternativeNames.InitializeEncode
title: IX509ExtensionAlternativeNames::InitializeEncode (certenroll.h)
description: Initializes the extension from an IAlternativeNames collection.
helpviewer_keywords: ["IX509ExtensionAlternativeNames interface [Security]","InitializeEncode method","IX509ExtensionAlternativeNames.InitializeEncode","IX509ExtensionAlternativeNames::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509ExtensionAlternativeNames interface","certenroll/IX509ExtensionAlternativeNames::InitializeEncode","security.ix509extensionalternativenames_initializeencode_method"]
old-location: security\ix509extensionalternativenames_initializeencode_method.htm
tech.root: security
ms.assetid: e520b2b4-c181-4fb1-98e8-f159bd0d31b4
ms.date: 12/05/2018
ms.keywords: IX509ExtensionAlternativeNames interface [Security],InitializeEncode method, IX509ExtensionAlternativeNames.InitializeEncode, IX509ExtensionAlternativeNames::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionAlternativeNames interface, certenroll/IX509ExtensionAlternativeNames::InitializeEncode, security.ix509extensionalternativenames_initializeencode_method
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
 - IX509ExtensionAlternativeNames::InitializeEncode
 - certenroll/IX509ExtensionAlternativeNames::InitializeEncode
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
 - IX509ExtensionAlternativeNames.InitializeEncode
---

# IX509ExtensionAlternativeNames::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the extension from an <a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a> collection.

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a> interface.

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
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

 The method associates the name collection with the XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and encodes it by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionalternativenames-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

 You can retrieve the following properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionalternativenames-get_alternativenames">AlternativeNames</a> property retrieves the collection of names (the raw extension data).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a>