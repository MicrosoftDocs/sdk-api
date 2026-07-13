---
UID: NF:certenroll.ICertPropertyFriendlyName.Initialize
title: ICertPropertyFriendlyName::Initialize (certenroll.h)
description: Initializes the object from the certificate display name.
helpviewer_keywords: ["ICertPropertyFriendlyName interface [Security]","Initialize method","ICertPropertyFriendlyName.Initialize","ICertPropertyFriendlyName::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyFriendlyName interface","certenroll/ICertPropertyFriendlyName::Initialize","security.icertpropertyfriendlyname_initialize_method"]
old-location: security\icertpropertyfriendlyname_initialize_method.htm
tech.root: security
ms.assetid: fb9a8108-f3d1-4a5c-bf3f-00002c085012
ms.date: 12/05/2018
ms.keywords: ICertPropertyFriendlyName interface [Security],Initialize method, ICertPropertyFriendlyName.Initialize, ICertPropertyFriendlyName::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyFriendlyName interface, certenroll/ICertPropertyFriendlyName::Initialize, security.icertpropertyfriendlyname_initialize_method
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
 - ICertPropertyFriendlyName::Initialize
 - certenroll/ICertPropertyFriendlyName::Initialize
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
 - ICertPropertyFriendlyName.Initialize
---

# ICertPropertyFriendlyName::Initialize


## -description

The <b>Initialize</b> method initializes the object from the certificate display name. This method is web enabled.

## -parameters

### -param strFriendlyName [in]

A <b>BSTR</b> variable that contains the name.  The string length cannot exceed 260 characters.

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

Typically, you specify the display name in a user interface or from the command line before beginning the enrollment process so that the name can be associated with the dummy certificate in the request store. To retrieve that value and use it here, call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname">CertificateFriendlyName</a> on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyfriendlyname-get_friendlyname">FriendlyName</a> property to retrieve the display name.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>