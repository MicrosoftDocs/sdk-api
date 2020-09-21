---
UID: NF:wincrypt.CertDuplicateStore
title: CertDuplicateStore function (wincrypt.h)
description: Duplicates a store handle by incrementing the store's reference count.
helpviewer_keywords: ["CertDuplicateStore","CertDuplicateStore function [Security]","_crypto2_certduplicatestore","security.certduplicatestore","wincrypt/CertDuplicateStore"]
old-location: security\certduplicatestore.htm
tech.root: security
ms.assetid: 628efd30-6e07-4748-82ac-5cdc723be451
ms.date: 12/05/2018
ms.keywords: CertDuplicateStore, CertDuplicateStore function [Security], _crypto2_certduplicatestore, security.certduplicatestore, wincrypt/CertDuplicateStore
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
 - CertDuplicateStore
 - wincrypt/CertDuplicateStore
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
 - CertDuplicateStore
---

# CertDuplicateStore function


## -description

The <b>CertDuplicateStore</b> function duplicates a store handle by incrementing the store's <a href="/windows/desktop/SecGloss/r-gly">reference count</a>.

## -parameters

### -param hCertStore [in]

A handle of the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> for which the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> is being incremented.

## -returns

Currently, a copy is not made of the handle, and the returned handle is the same as the handle that was input. If <b>NULL</b> is passed in, the called function will raise an access violation exception.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>