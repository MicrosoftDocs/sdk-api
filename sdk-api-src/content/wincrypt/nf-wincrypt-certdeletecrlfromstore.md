---
UID: NF:wincrypt.CertDeleteCRLFromStore
title: CertDeleteCRLFromStore function (wincrypt.h)
description: The CertDeleteCRLFromStore function deletes the specified certificate revocation list (CRL) context from the certificate store.
helpviewer_keywords: ["CertDeleteCRLFromStore","CertDeleteCRLFromStore function [Security]","_crypto2_certdeletecrlfromstore","security.certdeletecrlfromstore","wincrypt/CertDeleteCRLFromStore"]
old-location: security\certdeletecrlfromstore.htm
tech.root: security
ms.assetid: eb542c25-8d2b-4427-8f2a-719b472613a5
ms.date: 12/05/2018
ms.keywords: CertDeleteCRLFromStore, CertDeleteCRLFromStore function [Security], _crypto2_certdeletecrlfromstore, security.certdeletecrlfromstore, wincrypt/CertDeleteCRLFromStore
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
 - CertDeleteCRLFromStore
 - wincrypt/CertDeleteCRLFromStore
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
 - CertDeleteCRLFromStore
---

# CertDeleteCRLFromStore function


## -description

The <b>CertDeleteCRLFromStore</b> function deletes the specified <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context from the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

## -parameters

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure to be deleted.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One possible error code is the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The store was opened read-only, and a delete operation is not allowed.

</td>
</tr>
</table>

## -remarks

All subsequent get or find operations for the CRL in this store fail. However, memory allocated for the CRL is not freed until all duplicated contexts have also been freed.

The <i>pCrlContext</i> parameter is always freed by this function by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>, even for an error.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>