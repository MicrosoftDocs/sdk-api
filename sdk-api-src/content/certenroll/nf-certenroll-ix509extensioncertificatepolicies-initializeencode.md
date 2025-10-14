---
UID: NF:certenroll.IX509ExtensionCertificatePolicies.InitializeEncode
title: IX509ExtensionCertificatePolicies::InitializeEncode (certenroll.h)
description: Initializes the object from an ICertificatePolicies collection.
helpviewer_keywords: ["IX509ExtensionCertificatePolicies interface [Security]","InitializeEncode method","IX509ExtensionCertificatePolicies.InitializeEncode","IX509ExtensionCertificatePolicies::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509ExtensionCertificatePolicies interface","certenroll/IX509ExtensionCertificatePolicies::InitializeEncode","security.ix509extensioncertificatepolicies_initializeencode_method"]
old-location: security\ix509extensioncertificatepolicies_initializeencode_method.htm
tech.root: security
ms.assetid: 3134c668-afe6-447b-9f0e-8c21df36e131
ms.date: 12/05/2018
ms.keywords: IX509ExtensionCertificatePolicies interface [Security],InitializeEncode method, IX509ExtensionCertificatePolicies.InitializeEncode, IX509ExtensionCertificatePolicies::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionCertificatePolicies interface, certenroll/IX509ExtensionCertificatePolicies::InitializeEncode, security.ix509extensioncertificatepolicies_initializeencode_method
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
 - IX509ExtensionCertificatePolicies::InitializeEncode
 - certenroll/IX509ExtensionCertificatePolicies::InitializeEncode
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
 - IX509ExtensionCertificatePolicies.InitializeEncode
---

# IX509ExtensionCertificatePolicies::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the object from an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a> collection.

## -parameters

### -param pValue [in]

Pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a> interface.

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

 The method associates the name collection with the XCN_OID_CERT_POLICIES (2.5.29.32) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and encodes it by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensioncertificatepolicies-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object. You can retrieve the collection of policies (the raw data) by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensioncertificatepolicies-get_policies">Policies</a> property.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the extension OID.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensioncertificatepolicies-get_policies">Policies</a> property retrieves the collection of <a href="/windows/desktop/SecGloss/c-gly">certificate policies</a> (the raw extension data).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>