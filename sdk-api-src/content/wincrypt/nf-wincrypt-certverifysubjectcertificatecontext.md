---
UID: NF:wincrypt.CertVerifySubjectCertificateContext
title: CertVerifySubjectCertificateContext function (wincrypt.h)
description: The CertVerifySubjectCertificateContext function performs the enabled verification checks on a certificate by checking the validity of the certificate's issuer. The new Certificate Chain Verification Functions are recommended instead of this function.
helpviewer_keywords: ["CERT_STORE_REVOCATION_FLAG","CERT_STORE_SIGNATURE_FLAG","CERT_STORE_TIME_VALIDITY_FLAG","CertVerifySubjectCertificateContext","CertVerifySubjectCertificateContext function [Security]","_crypto2_certverifysubjectcertificatecontext","security.certverifysubjectcertificatecontext","wincrypt/CertVerifySubjectCertificateContext"]
old-location: security\certverifysubjectcertificatecontext.htm
tech.root: security
ms.assetid: 063b19cf-d3b3-4ec3-bfd3-9406eecd3e10
ms.date: 12/05/2018
ms.keywords: CERT_STORE_REVOCATION_FLAG, CERT_STORE_SIGNATURE_FLAG, CERT_STORE_TIME_VALIDITY_FLAG, CertVerifySubjectCertificateContext, CertVerifySubjectCertificateContext function [Security], _crypto2_certverifysubjectcertificatecontext, security.certverifysubjectcertificatecontext, wincrypt/CertVerifySubjectCertificateContext
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertVerifySubjectCertificateContext
 - wincrypt/CertVerifySubjectCertificateContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertVerifySubjectCertificateContext
---

# CertVerifySubjectCertificateContext function


## -description

The <b>CertVerifySubjectCertificateContext</b> function performs the enabled verification checks on a certificate by checking the validity of the certificate's issuer. The new 
<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a> are recommended instead of this function.

## -parameters

### -param pSubject [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure containing the subject's certificate.

### -param pIssuer [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> containing the issuer's certificate. When checking just CERT_STORE_TIME_VALIDITY_FLAG, <i>pIssuer</i> can be <b>NULL</b>.

### -param pdwFlags [in, out]

A pointer to a <b>DWORD</b> value contain verification check flags. The following flags can be set to enable verification checks on the subject certificate. They can be combined using a bitwise-<b>OR</b> operation to enable multiple verifications.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_REVOCATION_FLAG"></a><a id="cert_store_revocation_flag"></a><dl>
<dt><b>CERT_STORE_REVOCATION_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Checks whether the subject certificate is on the issuer's revocation list.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SIGNATURE_FLAG"></a><a id="cert_store_signature_flag"></a><dl>
<dt><b>CERT_STORE_SIGNATURE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Uses the public key in the issuer's certificate to verify the signature on the subject certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_TIME_VALIDITY_FLAG"></a><a id="cert_store_time_validity_flag"></a><dl>
<dt><b>CERT_STORE_TIME_VALIDITY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Gets the current time and verifies that it is within the subject certificate's validity period.

</td>
</tr>
</table>
 

If an enabled verification check succeeds, its flag is set to zero. If it fails, then its flag is set upon return.

If CERT_STORE_REVOCATION_FLAG was enabled and the issuer does not have a CRL in the store, then CERT_STORE_NO_CRL_FLAG is set in addition to CERT_STORE_REVOCATION_FLAG.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

For a verification check failure, <b>TRUE</b> is still returned. <b>FALSE</b> is returned only when a bad parameter is passed in.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One possible error code is the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An unsupported bit was set in <i>pdwFlags</i>. Any combination of CERT_STORE_SIGNATURE_FLAG, CERT_STORE_TIME_VALIDITY_FLAG, and CERT_STORE_REVOCATION_FLAG can be set. If <i>pIssuer</i> is <b>NULL</b>, only CERT_STORE_TIME_VALIDITY_FLAG can be set.

</td>
</tr>
</table>

## -remarks

The hexadecimal value of the flags can be combined using bitwise-<b>OR</b> operations to enable multiple verifications. For example, to enable both signature and time validity, the value


``` syntax
CERT_STORE_SIGNATURE_FLAG | CERT_STORE_TIME_VALIDITY_FLAG

```

is placed in the <i>pdwFlags</i> <b>DWORD</b> value as an input parameter. If CERT_STORE_SIGNATURE_FLAG verification succeeds, but CERT_STORE_TIME_VALIDITY_FLAG verification fails, <i>pdwFlags</i> is set to CERT_STORE_TIME_VALIDITY_FLAG when the function returns.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetissuercertificatefromstore">CertGetIssuerCertificateFromStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>
