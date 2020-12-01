---
UID: NF:wincrypt.CertDeleteCTLFromStore
title: CertDeleteCTLFromStore function (wincrypt.h)
description: The CertDeleteCTLFromStore function deletes the specified certificate trust list (CTL) context from a certificate store.
helpviewer_keywords: ["CertDeleteCTLFromStore","CertDeleteCTLFromStore function [Security]","_crypto2_certdeletectlfromstore","security.certdeletectlfromstore","wincrypt/CertDeleteCTLFromStore"]
old-location: security\certdeletectlfromstore.htm
tech.root: security
ms.assetid: e24d3445-8929-463a-b771-1f25f4e999b5
ms.date: 12/05/2018
ms.keywords: CertDeleteCTLFromStore, CertDeleteCTLFromStore function [Security], _crypto2_certdeletectlfromstore, security.certdeletectlfromstore, wincrypt/CertDeleteCTLFromStore
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
 - CertDeleteCTLFromStore
 - wincrypt/CertDeleteCTLFromStore
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
 - CertDeleteCTLFromStore
---

# CertDeleteCTLFromStore function


## -description

The <b>CertDeleteCTLFromStore</b> function deletes the specified <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context from a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

## -parameters

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure to be deleted.

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

All subsequent get or find operations for the CTL in this store fail. However, memory allocated for the CTL is not freed until all duplicated contexts have also been freed.

The <i>pCtlContext</i> parameter is always freed by this function by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>, even for an error.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>