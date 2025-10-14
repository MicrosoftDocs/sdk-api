---
UID: NF:certenroll.IPolicyQualifier.InitializeEncode
title: IPolicyQualifier::InitializeEncode (certenroll.h)
description: Initializes the object from a string and a value that identifies the qualifier type.
helpviewer_keywords: ["IPolicyQualifier interface [Security]","InitializeEncode method","IPolicyQualifier.InitializeEncode","IPolicyQualifier::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IPolicyQualifier interface","PolicyQualifierTypeUnknown","PolicyQualifierTypeUrl","PolicyQualifierTypeUserNotice","certenroll/IPolicyQualifier::InitializeEncode","security.ipolicyqualifier_initializeencode_method"]
old-location: security\ipolicyqualifier_initializeencode_method.htm
tech.root: security
ms.assetid: fc8b5916-0557-4f9b-8478-169a3dd9cebc
ms.date: 12/05/2018
ms.keywords: IPolicyQualifier interface [Security],InitializeEncode method, IPolicyQualifier.InitializeEncode, IPolicyQualifier::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IPolicyQualifier interface, PolicyQualifierTypeUnknown, PolicyQualifierTypeUrl, PolicyQualifierTypeUserNotice, certenroll/IPolicyQualifier::InitializeEncode, security.ipolicyqualifier_initializeencode_method
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
 - IPolicyQualifier::InitializeEncode
 - certenroll/IPolicyQualifier::InitializeEncode
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
 - IPolicyQualifier.InitializeEncode
---

# IPolicyQualifier::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the object from a string and a value that identifies the qualifier type.

## -parameters

### -param strQualifier [in]

A <b>BSTR</b> variable that contains the qualifier.

### -param Type [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-policyqualifiertype">PolicyQualifierType</a> enumeration value that specifies the type of qualifier applied to a certificate policy. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PolicyQualifierTypeUnknown"></a><a id="policyqualifiertypeunknown"></a><a id="POLICYQUALIFIERTYPEUNKNOWN"></a><dl>
<dt><b>PolicyQualifierTypeUnknown</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The qualifier type is not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyQualifierTypeUrl"></a><a id="policyqualifiertypeurl"></a><a id="POLICYQUALIFIERTYPEURL"></a><dl>
<dt><b>PolicyQualifierTypeUrl</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The qualifier is a URL that points to a Certification Practice Statement (CPS) that has been defined by the certification authority to outline the policies under which the certificate was issued and the purposes for which the certificate can be used.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyQualifierTypeUserNotice"></a><a id="policyqualifiertypeusernotice"></a><a id="POLICYQUALIFIERTYPEUSERNOTICE"></a><dl>
<dt><b>PolicyQualifierTypeUserNotice</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The qualifier is a text statement to be displayed by the application to any user who relies on the certificate. The user notice identifies the permitted uses of the certificate.

</td>
</tr>
</table>

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

If you specify <b>PolicyQualifierTypeUrl</b> in the <i>Type</i> parameter, this method associates the string entered in the <i>strQualifier</i> parameter with the <b>XCN_OID_PKIX_POLICY_QUALIFIER_CPS</b> (1.3.6.1.5.5.7.2.1) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and encodes it by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER). The URL is encoded as an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) IA5 string.

If you specify <b>PolicyQualifierTypeUserNotice</b> in the <i>Type</i> parameter, this method associates the string entered in the <i>strQualifier</i> parameter with the <b>XCN_OID_PKIX_POLICY_QUALIFIER_USERNOTICE</b> (1.3.6.1.5.5.7.2.2) OID and encodes it by using DER.

You can retrieve the following properties for this object:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_objectid">ObjectId</a> property retrieves an OID that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_qualifier">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <b>InitializeEncode</b> method.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_rawdata">RawData</a> property retrieves the DER-encoded qualifier.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_type">Type</a> property retrieves a value of the <a href="/windows/desktop/api/certenroll/ne-certenroll-policyqualifiertype">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>