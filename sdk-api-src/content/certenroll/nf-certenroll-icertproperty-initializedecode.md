---
UID: NF:certenroll.ICertProperty.InitializeDecode
title: ICertProperty::InitializeDecode (certenroll.h)
description: Initializes the object from a byte array that contains the property value.
helpviewer_keywords: ["ICertProperty interface [Security]","InitializeDecode method","ICertProperty.InitializeDecode","ICertProperty::InitializeDecode","InitializeDecode","InitializeDecode method [Security]","InitializeDecode method [Security]","ICertProperty interface","certenroll/ICertProperty::InitializeDecode","security.icertproperty_initializedecode_method"]
old-location: security\icertproperty_initializedecode_method.htm
tech.root: security
ms.assetid: 38b51242-cd4a-402e-b7ff-286f7bf66953
ms.date: 12/05/2018
ms.keywords: ICertProperty interface [Security],InitializeDecode method, ICertProperty.InitializeDecode, ICertProperty::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],ICertProperty interface, certenroll/ICertProperty::InitializeDecode, security.icertproperty_initializedecode_method
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
 - ICertProperty::InitializeDecode
 - certenroll/ICertProperty::InitializeDecode
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
 - ICertProperty.InitializeDecode
---

# ICertProperty::InitializeDecode


## -description

The <b>InitializeDecode</b> method initializes the object from a byte array that contains the property value. The byte array is represented by a Unicode-encoded string.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string.

### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded property value.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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

Specify the property to initialize by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-get_propertyid">PropertyId</a> property. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-get_rawdata">RawData</a> property to retrieve the encoded property value. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property value with a certificate.

If the <b>InitializeDecode</b> method fails, the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a> object is not initialized and the input property value is not saved. However, the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-get_propertyid">PropertyId</a> property retains the specified identifier.

The <b>InitializeDecode</b> method is provided to enable you to initialize custom properties and properties identified in the <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> enumeration for which there exist no specific interface. Each of the supported values in that enumeration contains information about the type of data, usually a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>, that you must supply to the <b>InitializeDecode</b> method. You can use the <a href="/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a> interface to convert a byte array to a string.

The following interfaces simplify creation of the most common properties:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchived">ICertPropertyArchived</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchivedkeyhash">ICertPropertyArchivedKeyHash</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyautoenroll">ICertPropertyAutoEnroll</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertybackedup">ICertPropertyBackedUp</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertykeyprovinfo">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrenewal">ICertPropertyRenewal</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrequestoriginator">ICertPropertyRequestOriginator</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertysha1hash">ICertPropertySHA1Hash</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>