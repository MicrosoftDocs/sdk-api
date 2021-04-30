---
UID: NF:wincrypt.CertGetCRLFromStore
title: CertGetCRLFromStore function (wincrypt.h)
description: Gets the first or next certificate revocation list (CRL) context from the certificate store for the specified issuer.
helpviewer_keywords: ["CERT_STORE_BASE_CRL_FLAG","CERT_STORE_DELTA_CRL_FLAG","CERT_STORE_SIGNATURE_FLAG","CERT_STORE_TIME_VALIDITY_FLAG","CertGetCRLFromStore","CertGetCRLFromStore function [Security]","_crypto2_certgetcrlfromstore","security.certgetcrlfromstore","wincrypt/CertGetCRLFromStore"]
old-location: security\certgetcrlfromstore.htm
tech.root: security
ms.assetid: 7bd21424-4f74-4bac-ab47-00d51ebdca1c
ms.date: 12/05/2018
ms.keywords: CERT_STORE_BASE_CRL_FLAG, CERT_STORE_DELTA_CRL_FLAG, CERT_STORE_SIGNATURE_FLAG, CERT_STORE_TIME_VALIDITY_FLAG, CertGetCRLFromStore, CertGetCRLFromStore function [Security], _crypto2_certgetcrlfromstore, security.certgetcrlfromstore, wincrypt/CertGetCRLFromStore
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
 - CertGetCRLFromStore
 - wincrypt/CertGetCRLFromStore
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
 - CertGetCRLFromStore
---

# CertGetCRLFromStore function


## -description

The <b>CertGetCRLFromStore</b> function gets the first or next <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) <a href="/windows/desktop/SecGloss/c-gly">context</a> from the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> for the specified issuer. The function also performs the enabled verification checks on the CRL. The new 
<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a> are recommended instead of this function.

## -parameters

### -param hCertStore [in]

Handle of a certificate store.

### -param pIssuerContext [in, optional]

A pointer to an issuer 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>. The <i>pIssuerContext</i> pointer can come from this store or another store, or could have been created by the calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a>. If <b>NULL</b> is passed for this parameter, all the CRLs in the store are found.

### -param pPrevCrlContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>. An issuer can have multiple CRLs. For example, it can generate delta CRLs by using an <a href="/windows/desktop/SecGloss/x-gly">X.509</a> version 3 extension. This parameter must be <b>NULL</b> on the first call to get the CRL. To get the next CRL for the issuer, the parameter is set to the <b>CRL_CONTEXT</b> returned by a previous call. A non-<b>NULL</b><i>pPrevCrlContext</i> is always freed by this function by calling <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>, even for an error.

### -param pdwFlags [in, out]

The following flag values are defined to enable verification checks on the returned CRL. These flags can be combined using a bitwise-<b>OR</b> operation. 




						

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_SIGNATURE_FLAG"></a><a id="cert_store_signature_flag"></a><dl>
<dt><b>CERT_STORE_SIGNATURE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Uses the public key in the issuer's certificate to verify the signature on the returned CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_TIME_VALIDITY_FLAG"></a><a id="cert_store_time_validity_flag"></a><dl>
<dt><b>CERT_STORE_TIME_VALIDITY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Gets the current time and verifies that it is within the time between the CRL's ThisUpdate and NextUpdate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_BASE_CRL_FLAG"></a><a id="cert_store_base_crl_flag"></a><dl>
<dt><b>CERT_STORE_BASE_CRL_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Gets a base CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_DELTA_CRL_FLAG"></a><a id="cert_store_delta_crl_flag"></a><dl>
<dt><b>CERT_STORE_DELTA_CRL_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Gets a delta CRL.

</td>
</tr>
</table>
 

If an enabled verification check succeeds, its flag is set to zero. 
						

If an enabled verification check fails, its flag remains set upon return. If <i>pIssuerContext</i> is <b>NULL</b>, then an enabled CERT_STORE_SIGNATURE_FLAG always fails and the CERT_STORE_NO_ISSUER_FLAG is also set. For more details, see  Remarks.

If only one of CERT_STORE_BASE_CRL_FLAG or CERT_STORE_DELTA_CRL_FLAG is set, this function returns either a base or delta CRL and the appropriate base or delta flag will be cleared on return. If both flags are set, only one of the flags will be cleared.

For a verification check failure, a pointer to the first or next 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> is still returned and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is not updated.

## -returns

If the function succeeds, the return value is a pointer to a read-only <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>.

If the function fails and the first or next CRL is not found, the return value is <b>NULL</b>.

The returned <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>. However, when the returned <b>CRL_CONTEXT</b> is supplied for <i>pPrevCrlContext</i> on a subsequent call, the function frees it.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the CRL context pointed to by the <i>pPrevCrlContext</i> parameter, or an unsupported flag was set in <i>pdwFlags</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Either no CRLs existed in the store for the issuer, or the function reached the end of the store's list.

</td>
</tr>
</table>

## -remarks

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a> can be called to make a duplicate CRL.

The hexadecimal values of the flags can be combined using a bitwise-<b>OR</b> operation to enable both verifications. For example, to enable both verifications, the <b>DWORD</b> value pointed to by <i>pdwFlags</i> is set to value CERT_STORE_SIGNATURE_FLAG | CERT_STORE_TIME_VALIDITY_FLAG. If the CERT_STORE_SIGNATURE_FLAG verification succeeded, but CERT_STORE_TIME_VALIDITY_FLAG verification failed, the <b>DWORD</b> value pointed to by <i>pdwFlags</i> is set to CERT_STORE_TIME_VALIDITY_FLAG when the function returns.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>