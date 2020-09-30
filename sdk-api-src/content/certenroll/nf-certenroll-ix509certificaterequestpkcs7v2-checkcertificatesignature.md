---
UID: NF:certenroll.IX509CertificateRequestPkcs7V2.CheckCertificateSignature
title: IX509CertificateRequestPkcs7V2::CheckCertificateSignature (certenroll.h)
description: Verifies the certificate signature.
helpviewer_keywords: ["CheckCertificateSignature","CheckCertificateSignature method [Security]","CheckCertificateSignature method [Security]","IX509CertificateRequestPkcs7V2 interface","IX509CertificateRequestPkcs7V2 interface [Security]","CheckCertificateSignature method","IX509CertificateRequestPkcs7V2.CheckCertificateSignature","IX509CertificateRequestPkcs7V2::CheckCertificateSignature","certenroll/IX509CertificateRequestPkcs7V2::CheckCertificateSignature","security.ix509certificaterequestpkcs7v2_checkcertificatesignature"]
old-location: security\ix509certificaterequestpkcs7v2_checkcertificatesignature.htm
tech.root: security
ms.assetid: 6ee30e16-1901-45dc-8023-ef605d8a4d21
ms.date: 12/05/2018
ms.keywords: CheckCertificateSignature, CheckCertificateSignature method [Security], CheckCertificateSignature method [Security],IX509CertificateRequestPkcs7V2 interface, IX509CertificateRequestPkcs7V2 interface [Security],CheckCertificateSignature method, IX509CertificateRequestPkcs7V2.CheckCertificateSignature, IX509CertificateRequestPkcs7V2::CheckCertificateSignature, certenroll/IX509CertificateRequestPkcs7V2::CheckCertificateSignature, security.ix509certificaterequestpkcs7v2_checkcertificatesignature
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateRequestPkcs7V2::CheckCertificateSignature
 - certenroll/IX509CertificateRequestPkcs7V2::CheckCertificateSignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509CertificateRequestPkcs7V2.CheckCertificateSignature
---

# IX509CertificateRequestPkcs7V2::CheckCertificateSignature


## -description

The <b>CheckCertificateSignature</b> method verifies the certificate signature.

## -parameters

### -param ValidateCertificateChain [in]

A Boolean value that specifies whether to also verify the certificate chain. This parameter can be <b>NULL</b>.

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
A signer certificate cannot be found.

</td>
</tr>
</table>

## -remarks

A PKCS #7 request has exactly one certificate-based signature.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7v2">IX509CertificateRequestPkcs7V2</a>