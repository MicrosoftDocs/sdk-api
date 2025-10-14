---
UID: NF:certenroll.IX509ExtensionEnhancedKeyUsage.InitializeEncode
title: IX509ExtensionEnhancedKeyUsage::InitializeEncode (certenroll.h)
description: Initializes the extension from a collection of IObjectId object identifiers (OIDs) that specify the intended uses of the public key.
helpviewer_keywords: ["IX509ExtensionEnhancedKeyUsage interface [Security]","InitializeEncode method","IX509ExtensionEnhancedKeyUsage.InitializeEncode","IX509ExtensionEnhancedKeyUsage::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509ExtensionEnhancedKeyUsage interface","certenroll/IX509ExtensionEnhancedKeyUsage::InitializeEncode","security.ix509extensionenhancedkeyusage_initializeencode_method"]
old-location: security\ix509extensionenhancedkeyusage_initializeencode_method.htm
tech.root: security
ms.assetid: 6cb12736-db5d-4d65-b32f-4bd11ceea01d
ms.date: 12/05/2018
ms.keywords: IX509ExtensionEnhancedKeyUsage interface [Security],InitializeEncode method, IX509ExtensionEnhancedKeyUsage.InitializeEncode, IX509ExtensionEnhancedKeyUsage::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionEnhancedKeyUsage interface, certenroll/IX509ExtensionEnhancedKeyUsage::InitializeEncode, security.ix509extensionenhancedkeyusage_initializeencode_method
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
 - IX509ExtensionEnhancedKeyUsage::InitializeEncode
 - certenroll/IX509ExtensionEnhancedKeyUsage::InitializeEncode
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
 - IX509ExtensionEnhancedKeyUsage.InitializeEncode
---

# IX509ExtensionEnhancedKeyUsage::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the extension from a collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>  object identifiers (OIDs) that specify the intended uses of the <a href="/windows/desktop/SecGloss/p-gly">public key</a>. This method is web enabled.

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> interface.

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

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionenhancedkeyusage-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the extension <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionenhancedkeyusage-get_enhancedkeyusage">EnhancedKeyUsage</a> property retrieves the collection of OIDs that identify the intended uses of the public key (the raw extension data).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>