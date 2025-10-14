---
UID: NF:certenroll.ICertPropertySHA1Hash.Initialize
title: ICertPropertySHA1Hash::Initialize (certenroll.h)
description: Initializes the object from the SHA-1 hash of a certificate.
helpviewer_keywords: ["ICertPropertySHA1Hash interface [Security]","Initialize method","ICertPropertySHA1Hash.Initialize","ICertPropertySHA1Hash::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertySHA1Hash interface","certenroll/ICertPropertySHA1Hash::Initialize","security.icertpropertysha1hash_initialize_method"]
old-location: security\icertpropertysha1hash_initialize_method.htm
tech.root: security
ms.assetid: 898da01b-94e6-4a07-9c53-f93378fbda8c
ms.date: 12/05/2018
ms.keywords: ICertPropertySHA1Hash interface [Security],Initialize method, ICertPropertySHA1Hash.Initialize, ICertPropertySHA1Hash::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertySHA1Hash interface, certenroll/ICertPropertySHA1Hash::Initialize, security.icertpropertysha1hash_initialize_method
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
 - ICertPropertySHA1Hash::Initialize
 - certenroll/ICertPropertySHA1Hash::Initialize
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
 - ICertPropertySHA1Hash.Initialize
---

# ICertPropertySHA1Hash::Initialize


## -description

The <b>Initialize</b> method initializes the object from the SHA-1 hash of a certificate.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the certificate hash.

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

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertysha1hash-get_sha1hash">SHA1Hash</a> property to retrieve the hash value.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertysha1hash">ICertPropertySHA1Hash</a>