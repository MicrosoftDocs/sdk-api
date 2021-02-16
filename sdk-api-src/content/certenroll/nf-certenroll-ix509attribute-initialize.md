---
UID: NF:certenroll.IX509Attribute.Initialize
title: IX509Attribute::Initialize (certenroll.h)
description: Initializes the object from an object identifier (OID) and a value.
helpviewer_keywords: ["IX509Attribute interface [Security]","Initialize method","IX509Attribute.Initialize","IX509Attribute::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509Attribute interface","certenroll/IX509Attribute::Initialize","security.ix509attribute_initialize_method"]
old-location: security\ix509attribute_initialize_method.htm
tech.root: security
ms.assetid: 82457ca3-4aae-4f47-950c-1146c8614a5b
ms.date: 12/05/2018
ms.keywords: IX509Attribute interface [Security],Initialize method, IX509Attribute.Initialize, IX509Attribute::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509Attribute interface, certenroll/IX509Attribute::Initialize, security.ix509attribute_initialize_method
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
 - IX509Attribute::Initialize
 - certenroll/IX509Attribute::Initialize
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
 - IX509Attribute.Initialize
---

# IX509Attribute::Initialize


## -description

The <b>Initialize</b> method initializes the object from  an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a value.

## -parameters

### -param pObjectId [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that contains the attribute OID.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the attribute value contained in the <i>strEncodedData</i> parameter.

### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the attribute value.

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
The pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromname">InitializeFromName</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromvalue">InitializeFromValue</a> methods before using it in this method.

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attribute-get_objectid">ObjectId</a> property to retrieve the OID. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attribute-get_rawdata">RawData</a> property to retrieve the attribute value.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>