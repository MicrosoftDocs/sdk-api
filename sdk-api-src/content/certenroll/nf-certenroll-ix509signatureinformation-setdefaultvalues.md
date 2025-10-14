---
UID: NF:certenroll.IX509SignatureInformation.SetDefaultValues
title: IX509SignatureInformation::SetDefaultValues (certenroll.h)
description: Specifies a default hashing algorithm used to create a digest of the certificate request prior to signing.
helpviewer_keywords: ["IX509SignatureInformation interface [Security]","SetDefaultValues method","IX509SignatureInformation.SetDefaultValues","IX509SignatureInformation::SetDefaultValues","SetDefaultValues","SetDefaultValues method [Security]","SetDefaultValues method [Security]","IX509SignatureInformation interface","certenroll/IX509SignatureInformation::SetDefaultValues","security.ix509signatureinformation_setdefaultvalues_method"]
old-location: security\ix509signatureinformation_setdefaultvalues_method.htm
tech.root: security
ms.assetid: 123e65e8-62bb-4bc7-9e15-113780be81e3
ms.date: 12/05/2018
ms.keywords: IX509SignatureInformation interface [Security],SetDefaultValues method, IX509SignatureInformation.SetDefaultValues, IX509SignatureInformation::SetDefaultValues, SetDefaultValues, SetDefaultValues method [Security], SetDefaultValues method [Security],IX509SignatureInformation interface, certenroll/IX509SignatureInformation::SetDefaultValues, security.ix509signatureinformation_setdefaultvalues_method
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
 - IX509SignatureInformation::SetDefaultValues
 - certenroll/IX509SignatureInformation::SetDefaultValues
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
 - IX509SignatureInformation.SetDefaultValues
---

# IX509SignatureInformation::SetDefaultValues


## -description

The <b>SetDefaultValues</b> method specifies a default hashing algorithm used to create a digest of the certificate request prior to  signing.



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
The hashing algorithm  OID could not be found.

</td>
</tr>
</table>

## -remarks

If the hash algorithm is already set, this method performs no action. If the hash algorithm has not been specified, this method sets it to XCN_OID_OIWSEC_sha1 and clears the signature algorithm cache.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
