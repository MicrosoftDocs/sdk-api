---
UID: NF:certenroll.ICertPropertyDescription.Initialize
title: ICertPropertyDescription::Initialize (certenroll.h)
description: Initializes the object from a string that contains descriptive information about the certificate.
old-location: security\icertpropertydescription_initialize_method.htm
tech.root: security
ms.assetid: 17e8ee9c-c861-4437-a70d-ccad6a5a293d
ms.date: 12/05/2018
ms.keywords: ICertPropertyDescription interface [Security],Initialize method, ICertPropertyDescription.Initialize, ICertPropertyDescription::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyDescription interface, certenroll/ICertPropertyDescription::Initialize, security.icertpropertydescription_initialize_method
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
 - ICertPropertyDescription::Initialize
 - certenroll/ICertPropertyDescription::Initialize
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
 - ICertPropertyDescription.Initialize
---

# ICertPropertyDescription::Initialize


## -description

The <b>Initialize</b> method initializes the object from a string that contains descriptive information about the certificate. Use this property to create a string that can be displayed in user interfaces that enumerate certificate properties. This method is web enabled.

## -parameters

### -param strDescription [in]

A <b>BSTR</b> variable that contains a description. The string length cannot exceed 260 characters.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILENAME_EXCED_RANGE)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The string length exceeds 260 characters.

</td>
</tr>
</table>

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertydescription-get_description">Description</a> property to retrieve the description string.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>