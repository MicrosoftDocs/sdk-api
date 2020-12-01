---
UID: NF:wincrypt.CertFreeCTLContext
title: CertFreeCTLContext function (wincrypt.h)
description: Frees a certificate trust list (CTL) context by decrementing its reference count.
helpviewer_keywords: ["CertFreeCTLContext","CertFreeCTLContext function [Security]","_crypto2_certfreectlcontext","security.certfreectlcontext","wincrypt/CertFreeCTLContext"]
old-location: security\certfreectlcontext.htm
tech.root: security
ms.assetid: 84b1aa0c-44d9-4a2f-861c-fa7d8caac192
ms.date: 12/05/2018
ms.keywords: CertFreeCTLContext, CertFreeCTLContext function [Security], _crypto2_certfreectlcontext, security.certfreectlcontext, wincrypt/CertFreeCTLContext
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
 - CertFreeCTLContext
 - wincrypt/CertFreeCTLContext
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
 - CertFreeCTLContext
---

# CertFreeCTLContext function


## -description

The <b>CertFreeCTLContext</b> function frees a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) <a href="/windows/desktop/SecGloss/c-gly">context</a> by decrementing its <a href="/windows/desktop/SecGloss/r-gly">reference count</a>. When the reference count goes to zero, <b>CertFreeCTLContext</b> frees the memory used by a CTL context.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.

## -parameters

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> to be freed.

## -returns

The function always returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>