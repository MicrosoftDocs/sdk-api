---
UID: NF:certenroll.IX509ExtensionMSApplicationPolicies.InitializeDecode
title: IX509ExtensionMSApplicationPolicies::InitializeDecode (certenroll.h)
description: Initializes the extension from a Distinguished Encoding Rules (DER) encoded byte array that contains the extension value. (IX509ExtensionMSApplicationPolicies.InitializeDecode)
helpviewer_keywords: ["IX509ExtensionMSApplicationPolicies interface [Security]","InitializeDecode method","IX509ExtensionMSApplicationPolicies.InitializeDecode","IX509ExtensionMSApplicationPolicies::InitializeDecode","InitializeDecode","InitializeDecode method [Security]","InitializeDecode method [Security]","IX509ExtensionMSApplicationPolicies interface","certenroll/IX509ExtensionMSApplicationPolicies::InitializeDecode","security.ix509extensionmsapplicationpolicies_initializedecode_method"]
old-location: security\ix509extensionmsapplicationpolicies_initializedecode_method.htm
tech.root: security
ms.assetid: b99d756c-01fd-4bde-a64b-c908626e9190
ms.date: 12/05/2018
ms.keywords: IX509ExtensionMSApplicationPolicies interface [Security],InitializeDecode method, IX509ExtensionMSApplicationPolicies.InitializeDecode, IX509ExtensionMSApplicationPolicies::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509ExtensionMSApplicationPolicies interface, certenroll/IX509ExtensionMSApplicationPolicies::InitializeDecode, security.ix509extensionmsapplicationpolicies_initializedecode_method
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
 - IX509ExtensionMSApplicationPolicies::InitializeDecode
 - certenroll/IX509ExtensionMSApplicationPolicies::InitializeDecode
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
 - IX509ExtensionMSApplicationPolicies.InitializeDecode
---

# IX509ExtensionMSApplicationPolicies::InitializeDecode


## -description

The <b>InitializeDecode</b> method initializes the  extension from a <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value. The encoded byte array is represented by a Unicode encoded string.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the <i>strEncodedData</i> value.

### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded extension.

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

 You can use this method if you have a DER-encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) object that contains a <b>CertificatePolicies</b> extension. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a> interface.

You must call either <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionmsapplicationpolicies-initializeencode">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionmsapplicationpolicies">IX509ExtensionMSApplicationPolicies</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the extension <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionmsapplicationpolicies-get_policies">Policies</a> property retrieves the collection of <a href="/windows/desktop/SecGloss/c-gly">certificate policies</a> (the raw extension data).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionmsapplicationpolicies">IX509ExtensionMSApplicationPolicies</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionmsapplicationpolicies-initializeencode">InitializeEncode</a>
