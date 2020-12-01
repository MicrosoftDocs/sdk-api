---
UID: NF:wincrypt.CertGetIssuerCertificateFromStore
title: CertGetIssuerCertificateFromStore function (wincrypt.h)
description: Retrieves the certificate context from the certificate store for the first or next issuer of the specified subject certificate. The new Certificate Chain Verification Functions are recommended instead of the use of this function.
helpviewer_keywords: ["CERT_STORE_NO_CRL_FLAG","CERT_STORE_NO_ISSUER_FLAG","CERT_STORE_REVOCATION_FLAG","CERT_STORE_SIGNATURE_FLAG","CERT_STORE_TIME_VALIDITY_FLAG","CertGetIssuerCertificateFromStore","CertGetIssuerCertificateFromStore function [Security]","_crypto2_certgetissuercertificatefromstore","security.certgetissuercertificatefromstore","wincrypt/CertGetIssuerCertificateFromStore"]
old-location: security\certgetissuercertificatefromstore.htm
tech.root: security
ms.assetid: b57982d0-cba8-43cd-a544-3635fdf599e2
ms.date: 12/05/2018
ms.keywords: CERT_STORE_NO_CRL_FLAG, CERT_STORE_NO_ISSUER_FLAG, CERT_STORE_REVOCATION_FLAG, CERT_STORE_SIGNATURE_FLAG, CERT_STORE_TIME_VALIDITY_FLAG, CertGetIssuerCertificateFromStore, CertGetIssuerCertificateFromStore function [Security], _crypto2_certgetissuercertificatefromstore, security.certgetissuercertificatefromstore, wincrypt/CertGetIssuerCertificateFromStore
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
 - CertGetIssuerCertificateFromStore
 - wincrypt/CertGetIssuerCertificateFromStore
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
 - CertGetIssuerCertificateFromStore
---

# CertGetIssuerCertificateFromStore function


## -description

The <b>CertGetIssuerCertificateFromStore</b> function retrieves the certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> from the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> for the first or next issuer of the specified subject certificate. The new 
<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a> are recommended instead of the use of this function.

## -parameters

### -param hCertStore [in]

Handle of a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param pSubjectContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the subject information. This parameter can be obtained from any certificate store or can be created by the calling application using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a> function.

### -param pPrevIssuerContext [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the issuer information. An issuer can have multiple certificates, especially when a validity period is about to change. This parameter must be <b>NULL</b> on the call to get the first issuer certificate. To get the next certificate for the issuer, set <i>pPrevIssuerContext</i> to the <b>CERT_CONTEXT</b> structure returned by the previous call. 

This function frees the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> referenced by non-<b>NULL</b> values of this parameter.

### -param pdwFlags [in, out]

The following flags enable verification checks on the returned certificate. They can be combined using a bitwise-<b>OR</b> operation to enable multiple verifications. 




						
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_NO_CRL_FLAG"></a><a id="cert_store_no_crl_flag"></a><dl>
<dt><b>CERT_STORE_NO_CRL_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Indicates no matching CRL was found.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_NO_ISSUER_FLAG"></a><a id="cert_store_no_issuer_flag"></a><dl>
<dt><b>CERT_STORE_NO_ISSUER_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Indicates no issuer certificate was found.

</td>
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
 

If a verification check of an enabled type succeeds, its flag is set to zero. If it fails, its flag remains set upon return. For CERT_STORE_REVOCATION_FLAG, the verification succeeds if the function does not find a CRL related to the subject certificate.

If CERT_STORE_REVOCATION_FLAG is set and the issuer does not have a CRL in the store, CERT_STORE_NO_CRL_FLAG is set and CERT_STORE_REVOCATION_FLAG remains set.

If CERT_STORE_SIGNATURE_FLAG or CERT_STORE_REVOCATION_FLAG is set, CERT_STORE_NO_ISSUER_FLAG is set if the function does not find an issuer certificate in the store. For more details, see  Remarks.

In the case of a verification check failure, a pointer to the issuer's 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> is still returned and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is not updated.

## -returns

If the function succeeds, the return value is a pointer to a read-only issuer <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>.

If the function fails and the first or next issuer certificate is not found, the return value is <b>NULL</b>.

Only the last returned <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. When the returned <b>CERT_CONTEXT</b> from one call to the function is supplied as the <i>pPrevIssuerContext</i> parameter on a subsequent call, the context is freed as part of the action of the function.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No issuer was found for the subject certificate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_SELF_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
The issuer certificate is the same as the subject certificate. It is a self-signed <a href="/windows/desktop/SecGloss/r-gly">root certificate</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that of the certificate context pointed to by the <i>pPrevIssuerContext</i> parameter, or an unsupported flag was set in <i>pdwFlags</i>.

</td>
</tr>
</table>

## -remarks

The returned pointer is freed when passed as the <i>pPrevIssuerContext</i> parameter on a subsequent call to the function. Otherwise, the pointer must be explicitly freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. A <i>pPrevIssuerContext</i> that is not <b>NULL</b> is always freed by <b>CertGetIssuerCertificateFromStore</b> using a call to <b>CertFreeCertificateContext</b>, even if there is an error in the function.


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a> can be called to make a duplicate of the issuer certificate.

The hexadecimal values for <i>dwFlags</i> can be combined using a bitwise-<b>OR</b> operation to enable multiple verifications. For example, to enable both signature and time validity, the value 0x00000003 is passed in <i>dwFlags</i> on input. In this case, if CERT_STORE_SIGNATURE_FLAG verification succeeds but CERT_STORE_TIME_VALIDITY_FLAG verification fails, <i>dwFlags</i> returns as 0x00000002 on output.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>