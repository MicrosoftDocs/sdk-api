---
UID: NF:certenroll.IX509Extension.Initialize
title: IX509Extension::Initialize (certenroll.h)
description: Initializes an IX509Extension object by using an object identifier (OID) and a byte array that contains the Distinguished Encoding Rules (DER) encoded extension.
helpviewer_keywords: ["IX509Extension interface [Security]","Initialize method","IX509Extension.Initialize","IX509Extension::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509Extension interface","certenroll/IX509Extension::Initialize","security.ix509extension_initialize_method"]
old-location: security\ix509extension_initialize_method.htm
tech.root: security
ms.assetid: a01a371b-7dc2-4204-8029-269ac4a9c0d5
ms.date: 12/05/2018
ms.keywords: IX509Extension interface [Security],Initialize method, IX509Extension.Initialize, IX509Extension::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509Extension interface, certenroll/IX509Extension::Initialize, security.ix509extension_initialize_method
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
 - IX509Extension::Initialize
 - certenroll/IX509Extension::Initialize
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
 - IX509Extension.Initialize
---

# IX509Extension::Initialize


## -description

The <b>Initialize</b> method initializes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a> object by using an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a byte array that contains the <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded extension. The DER-encoded byte array is represented by a Unicode-encoded string. This method is web enabled.

## -parameters

### -param pObjectId [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that contains the extension OID.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string.

### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded extension value.

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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The OID could not be found.

</td>
</tr>
</table>

## -remarks

A certificate extension consists of an OID, a Boolean value that identifies whether the extension is critical, and a byte array that contains the extension value. The extension is defined by an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard and is encoded by using DER. You must specify  the DER-encoded byte array as a string that is either a pure binary sequence or is Unicode encoded. You can specify the type of encoding to apply to the string by using the <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>