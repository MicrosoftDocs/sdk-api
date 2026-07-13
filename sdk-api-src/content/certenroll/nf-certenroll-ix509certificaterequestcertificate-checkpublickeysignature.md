---
UID: NF:certenroll.IX509CertificateRequestCertificate.CheckPublicKeySignature
title: IX509CertificateRequestCertificate::CheckPublicKeySignature (certenroll.h)
description: Verifies the certificate signature by using the public key of the signing certificate.
helpviewer_keywords: ["CheckPublicKeySignature","CheckPublicKeySignature method [Security]","CheckPublicKeySignature method [Security]","IX509CertificateRequestCertificate interface","IX509CertificateRequestCertificate interface [Security]","CheckPublicKeySignature method","IX509CertificateRequestCertificate.CheckPublicKeySignature","IX509CertificateRequestCertificate::CheckPublicKeySignature","certenroll/IX509CertificateRequestCertificate::CheckPublicKeySignature","security.ix509certificaterequestcertificate_checkpublickeysignature_method"]
old-location: security\ix509certificaterequestcertificate_checkpublickeysignature_method.htm
tech.root: security
ms.assetid: b7c7becc-667a-4ee2-ae61-0a009d0c87e7
ms.date: 12/05/2018
ms.keywords: CheckPublicKeySignature, CheckPublicKeySignature method [Security], CheckPublicKeySignature method [Security],IX509CertificateRequestCertificate interface, IX509CertificateRequestCertificate interface [Security],CheckPublicKeySignature method, IX509CertificateRequestCertificate.CheckPublicKeySignature, IX509CertificateRequestCertificate::CheckPublicKeySignature, certenroll/IX509CertificateRequestCertificate::CheckPublicKeySignature, security.ix509certificaterequestcertificate_checkpublickeysignature_method
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
 - IX509CertificateRequestCertificate::CheckPublicKeySignature
 - certenroll/IX509CertificateRequestCertificate::CheckPublicKeySignature
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
 - IX509CertificateRequestCertificate.CheckPublicKeySignature
---

# IX509CertificateRequestCertificate::CheckPublicKeySignature


## -description

The <b>CheckPublicKeySignature</b> method verifies the certificate signature by using the public key of the signing certificate.

## -parameters

### -param pPublicKey [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> interface that represents the public key.

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
<dt><b>CRYPT_E_NO_SIGNER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The signature cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> object has not been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object has not been initialized.

</td>
</tr>
</table>

## -remarks

This method decrypts the signature and compares it to a hash of the certificate, using the hash algorithm specified by the signature. You must initialize the request object before calling this property. For more information, see any of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>