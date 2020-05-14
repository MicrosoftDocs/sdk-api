---
UID: NF:certenroll.IX509ExtensionBasicConstraints.InitializeEncode
title: IX509ExtensionBasicConstraints::InitializeEncode (certenroll.h)
description: Initializes the extension from a Boolean value that indicates whether the certificate subject is a certification authority (CA) and an integer that contains the depth of the subordinate CA chain.helpviewer_keywords: ["IX509ExtensionBasicConstraints interface [Security]","InitializeEncode method","IX509ExtensionBasicConstraints.InitializeEncode","IX509ExtensionBasicConstraints::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509ExtensionBasicConstraints interface","certenroll/IX509ExtensionBasicConstraints::InitializeEncode","security.ix509extensionbasicconstraints_initializeencode_method"]
old-location: security\ix509extensionbasicconstraints_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: e9a08445-8fc5-45cc-a2c6-ec62470e5c55
ms.date: 12/05/2018
ms.keywords: IX509ExtensionBasicConstraints interface [Security],InitializeEncode method, IX509ExtensionBasicConstraints.InitializeEncode, IX509ExtensionBasicConstraints::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionBasicConstraints interface, certenroll/IX509ExtensionBasicConstraints::InitializeEncode, security.ix509extensionbasicconstraints_initializeencode_method
f1_keywords:
- certenroll/IX509ExtensionBasicConstraints.InitializeEncode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IX509ExtensionBasicConstraints.InitializeEncode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionBasicConstraints::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a Boolean value that indicates whether the certificate subject is a certification authority (CA) and an integer that contains the depth of the subordinate CA chain.


## -parameters




### -param IsCA [in]

A <b>VARIANT_BOOL</b> variable that specifies whether the certificate subject is a CA.


### -param PathLenConstraint [in]

A <b>LONG</b> variable that contains the maximum number of certificates in the chain.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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



 The method associates the name collection with the XCN_OID_BASIC_CONSTRAINTS2 (2.5.29.19) <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and encodes it by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-initializedecode">InitializeDecode</a> before you can use an  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-get_isca">IsCA</a> property identifies whether the certificate subject can be a certification authority.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-get_pathlenconstraint">PathLenConstraint</a> property identifies the depth of the subordinate certification authority chain.</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a>
 

 

