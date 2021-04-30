---
UID: NF:wincrypt.CertEnumCTLsInStore
title: CertEnumCTLsInStore function (wincrypt.h)
description: The CertEnumCTLsInStore function retrieves the first or next certificate trust list (CTL) context in a certificate store. Used in a loop, this function can retrieve in sequence all CTL contexts in a certificate store.
helpviewer_keywords: ["CertEnumCTLsInStore","CertEnumCTLsInStore function [Security]","_crypto2_certenumctlsinstore","security.certenumctlsinstore","wincrypt/CertEnumCTLsInStore"]
old-location: security\certenumctlsinstore.htm
tech.root: security
ms.assetid: dac9f91e-8ed4-43ce-8147-485c2ed7edd5
ms.date: 12/05/2018
ms.keywords: CertEnumCTLsInStore, CertEnumCTLsInStore function [Security], _crypto2_certenumctlsinstore, security.certenumctlsinstore, wincrypt/CertEnumCTLsInStore
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
 - CertEnumCTLsInStore
 - wincrypt/CertEnumCTLsInStore
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
 - CertEnumCTLsInStore
---

# CertEnumCTLsInStore function


## -description

The <b>CertEnumCTLsInStore</b> function retrieves the first or next <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. Used in a loop, this function can retrieve in sequence all CTL contexts in a certificate store.

## -parameters

### -param hCertStore [in]

Handle of a certificate store.

### -param pPrevCtlContext [in]

A pointer to the previous 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure found. It must be <b>NULL</b> to get the first CTL in the store. Successive CTLs are enumerated by setting <i>pPrevCtlContext</i> to the pointer returned by a previous call. This function frees the <b>CTL_CONTEXT</b> referenced by non-<b>NULL</b> values of this parameter. The enumeration skips any CTLs previously deleted by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletectlfromstore">CertDeleteCTLFromStore</a>.

## -returns

If the function succeeds, the return value is a pointer to a read-only 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>.

If the function fails and a CTL is not found, the return value is <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Some possible error codes follow.

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
Either no CTLs exist in the store, or the function reached the end of the store's list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the CTL context pointed to by the <i>pPrevCtlContext</i> parameter.

</td>
</tr>
</table>

## -remarks

The returned pointer is freed when passed as the <i>pPrevCtlContext</i> on a subsequent call. Otherwise, the pointer must be explicitly freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>. A <i>pPrevCtlContext</i> that is not <b>NULL</b> is always freed by this function (through a call to <b>CertFreeCTLContext</b>), even for an error.

A duplicate can be made by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatectlcontext">CertDuplicateCTLContext</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletectlfromstore">CertDeleteCTLFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatectlcontext">CertDuplicateCTLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>