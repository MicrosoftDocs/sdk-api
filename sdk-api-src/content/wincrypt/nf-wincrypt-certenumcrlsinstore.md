---
UID: NF:wincrypt.CertEnumCRLsInStore
title: CertEnumCRLsInStore function (wincrypt.h)
description: The CertEnumCRLsInStore function retrieves the first or next certificate revocation list (CRL) context in a certificate store. Used in a loop, this function can retrieve in sequence all CRL contexts in a certificate store.
helpviewer_keywords: ["CertEnumCRLsInStore","CertEnumCRLsInStore function [Security]","_crypto2_certenumcrlsinstore","security.certenumcrlsinstore","wincrypt/CertEnumCRLsInStore"]
old-location: security\certenumcrlsinstore.htm
tech.root: security
ms.assetid: fc25ca04-8520-4053-9591-afc81c88670c
ms.date: 12/05/2018
ms.keywords: CertEnumCRLsInStore, CertEnumCRLsInStore function [Security], _crypto2_certenumcrlsinstore, security.certenumcrlsinstore, wincrypt/CertEnumCRLsInStore
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
 - CertEnumCRLsInStore
 - wincrypt/CertEnumCRLsInStore
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
 - CertEnumCRLsInStore
---

# CertEnumCRLsInStore function


## -description

The <b>CertEnumCRLsInStore</b> function retrieves the first or next <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. Used in a loop, this function can retrieve in sequence all CRL contexts in a certificate store.

## -parameters

### -param hCertStore [in]

Handle of a certificate store.

### -param pPrevCrlContext [in]

A pointer to the previous 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure found. The <i>pPrevCrlContext</i> parameter must be <b>NULL</b> to get the first CRL in the store. Successive CRLs are enumerated by setting <i>pPrevCrlContext</i> to the pointer returned by a previous call to the function.  This function frees the <b>CRL_CONTEXT</b> referenced by non-<b>NULL</b> values of this parameter. The enumeration skips any CRLs previously deleted by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a>.

## -returns

If the function succeeds, the return value is a pointer to the next 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> in the store.

<b>NULL</b> is returned if the function fails. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

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
The handle in the <i>hCertStore</i> parameter is not the same as that in the certificate context pointed to by <i>pPrevCrlContext</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No CRL was found. This happens if the store is empty or the end of the store's list is reached.

</td>
</tr>
</table>

## -remarks

The returned pointer is freed when it is passed as the <i>pPrevCrlContext</i> on a subsequent call to the function. Otherwise, the pointer must explicitly be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>. A <i>pPrevCrlContext</i> that is not <b>NULL</b> is always freed when passed to this function through a call to <b>CertFreeCRLContext</b>, even if the function itself returns an error.

A duplicate of the CRL <a href="/windows/desktop/SecGloss/c-gly">context</a> returned by this function can be made by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcrlinstore">CertFindCRLInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>