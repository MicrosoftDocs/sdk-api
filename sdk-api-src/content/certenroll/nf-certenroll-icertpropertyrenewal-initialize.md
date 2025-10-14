---
UID: NF:certenroll.ICertPropertyRenewal.Initialize
title: ICertPropertyRenewal::Initialize (certenroll.h)
description: Initializes the object from a SHA-1 hash of the new certificate.
helpviewer_keywords: ["ICertPropertyRenewal interface [Security]","Initialize method","ICertPropertyRenewal.Initialize","ICertPropertyRenewal::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyRenewal interface","certenroll/ICertPropertyRenewal::Initialize","security.icertpropertyrenewal_initialize_method"]
old-location: security\icertpropertyrenewal_initialize_method.htm
tech.root: security
ms.assetid: dc1e124e-400a-4f1e-8e87-095b6a3341d4
ms.date: 12/05/2018
ms.keywords: ICertPropertyRenewal interface [Security],Initialize method, ICertPropertyRenewal.Initialize, ICertPropertyRenewal::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyRenewal interface, certenroll/ICertPropertyRenewal::Initialize, security.icertpropertyrenewal_initialize_method
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
 - ICertPropertyRenewal::Initialize
 - certenroll/ICertPropertyRenewal::Initialize
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
 - ICertPropertyRenewal.Initialize
---

# ICertPropertyRenewal::Initialize


## -description

The <b>Initialize</b> method initializes the object from a SHA-1 hash of the new certificate.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the hash.

### -param strRenewalValue [in]

A <b>BSTR</b> variable that contains the hash.

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

Typically this property is initialized during the enrollment process. You can retrieve the certificate used during enrollment by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_certificate">Certificate</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrenewal-get_renewal">Renewal</a> property to retrieve the hash.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrenewal">ICertPropertyRenewal</a>