---
UID: NF:wincrypt.CertDuplicateCTLContext
title: CertDuplicateCTLContext function (wincrypt.h)
description: The CertDuplicateCTLContext function duplicates a certificate trust list (CTL) context by incrementing its reference count.
helpviewer_keywords: ["CertDuplicateCTLContext","CertDuplicateCTLContext function [Security]","_crypto2_certduplicatectlcontext","security.certduplicatectlcontext","wincrypt/CertDuplicateCTLContext"]
old-location: security\certduplicatectlcontext.htm
tech.root: security
ms.assetid: 512d246f-9f22-4ac1-a4fc-d5c615a65cf9
ms.date: 12/05/2018
ms.keywords: CertDuplicateCTLContext, CertDuplicateCTLContext function [Security], _crypto2_certduplicatectlcontext, security.certduplicatectlcontext, wincrypt/CertDuplicateCTLContext
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
 - CertDuplicateCTLContext
 - wincrypt/CertDuplicateCTLContext
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
 - CertDuplicateCTLContext
---

# CertDuplicateCTLContext function


## -description

The <b>CertDuplicateCTLContext</b> function duplicates a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context by incrementing its <a href="/windows/desktop/SecGloss/r-gly">reference count</a>.

## -parameters

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure for which the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> is being incremented.

## -returns

Currently, a copy is not made of the context, and the returned pointer to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> is the same as pointer input. If the pointer passed into this function is <b>NULL</b>, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>