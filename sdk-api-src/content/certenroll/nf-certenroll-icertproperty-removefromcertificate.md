---
UID: NF:certenroll.ICertProperty.RemoveFromCertificate
title: ICertProperty::RemoveFromCertificate (certenroll.h)
description: Disassociates a property from a certificate.
helpviewer_keywords: ["ICertProperty interface [Security]","RemoveFromCertificate method","ICertProperty.RemoveFromCertificate","ICertProperty::RemoveFromCertificate","RemoveFromCertificate","RemoveFromCertificate method [Security]","RemoveFromCertificate method [Security]","ICertProperty interface","certenroll/ICertProperty::RemoveFromCertificate","security.icertproperty_removefromcertificate_method"]
old-location: security\icertproperty_removefromcertificate_method.htm
tech.root: security
ms.assetid: 9f3e21ec-f537-40ba-84a3-b71c7aa50e84
ms.date: 12/05/2018
ms.keywords: ICertProperty interface [Security],RemoveFromCertificate method, ICertProperty.RemoveFromCertificate, ICertProperty::RemoveFromCertificate, RemoveFromCertificate, RemoveFromCertificate method [Security], RemoveFromCertificate method [Security],ICertProperty interface, certenroll/ICertProperty::RemoveFromCertificate, security.icertproperty_removefromcertificate_method
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
 - ICertProperty::RemoveFromCertificate
 - certenroll/ICertProperty::RemoveFromCertificate
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
 - ICertProperty.RemoveFromCertificate
---

# ICertProperty::RemoveFromCertificate


## -description

The <b>RemoveFromCertificate</b> method disassociates a property from a certificate. Specify the property to remove by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-get_propertyid">PropertyId</a> property.

## -parameters

### -param MachineContext [in]

A <b>VARIANT_BOOL</b> value that indicates  whether the certificate store is located on the local computer. Specify <b>VARIANT_TRUE</b> if the store is local.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of encoding applied to  the certificate string identified by the <i>strCertificate</i> parameter.

### -param strCertificate [in]

A <b>BSTR</b> variable that contains the DER-encoded certificate.

Beginning with Windows 7 and Windows Server 2008 R2, you can specify a certificate thumb print or serial number rather than an encoded certificate. Doing so causes the function to search the appropriate local stores for the matching certificate. Keep in mind the following points:

<ul>
<li>The <b>BSTR</b> must be an even number of hexadecimal digits.</li>
<li>Whitespace between hexadecimal pairs is ignored.</li>
<li>The <i>Encoding</i> parameter must be set to <b>XCN_CRYPT_STRING_HEXRAW</b>.</li>
<li>The <i>MachineContext</i> parameter determines whether the user or computer stores or both are searched.</li>
<li>If a private key is needed, only the personal and request stores are searched.</li>
<li>If a private key is not needed, the root and intermediate CA stores are also searched.</li>
</ul>

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
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_MSG_TYPE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate was found but the private key could not be loaded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>