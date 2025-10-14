---
UID: NF:certenroll.IX509PublicKey.Initialize
title: IX509PublicKey::Initialize (certenroll.h)
description: Initializes the object from a public key algorithm object identifier (OID) and from byte arrays that contain a public key and the associated parameters, if any.
helpviewer_keywords: ["IX509PublicKey interface [Security]","Initialize method","IX509PublicKey.Initialize","IX509PublicKey::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509PublicKey interface","certenroll/IX509PublicKey::Initialize","security.ix509publickey_initialize_method"]
old-location: security\ix509publickey_initialize_method.htm
tech.root: security
ms.assetid: b6db46b2-95f5-4ba9-829d-97bf83fd9806
ms.date: 12/05/2018
ms.keywords: IX509PublicKey interface [Security],Initialize method, IX509PublicKey.Initialize, IX509PublicKey::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509PublicKey interface, certenroll/IX509PublicKey::Initialize, security.ix509publickey_initialize_method
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
 - IX509PublicKey::Initialize
 - certenroll/IX509PublicKey::Initialize
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
 - IX509PublicKey.Initialize
---

# IX509PublicKey::Initialize


## -description

The <b>Initialize</b> method initializes the object from a public key  algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and from byte arrays that contain a public key and the associated parameters, if any. The byte arrays are represented by Unicode-encoded strings.

## -parameters

### -param pObjectId [in]

Pointer to an  <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents the algorithm OID.

### -param strEncodedKey [in]

A <b>BSTR</b> variable that contains the public key.

### -param strEncodedParameters [in]

A <b>BSTR</b> variable that contains the parameters associated with the public key. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-get_encodedparameters">EncodedParameters</a> property.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  arguments specified in the <i>strEncodedKey</i> and <i>strEncodedParameters</i> parameters. The default value is XCN_CRYPT_STRING_BASE64.

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

The <b>Initialize</b> method initializes the following property values:

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