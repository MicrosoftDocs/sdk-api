---
UID: NF:wincrypt.CryptMemAlloc
title: CryptMemAlloc function (wincrypt.h)
description: The CryptMemAlloc function allocates memory for a buffer. It is used by all Crypt32.lib functions that return allocated buffers.
helpviewer_keywords: ["CryptMemAlloc","CryptMemAlloc function [Security]","_crypto2_cryptmemalloc","security.cryptmemalloc","wincrypt/CryptMemAlloc"]
old-location: security\cryptmemalloc.htm
tech.root: security
ms.assetid: ac7588b1-ff8c-4f8d-a8ab-f0e8a18e5614
ms.date: 12/05/2018
ms.keywords: CryptMemAlloc, CryptMemAlloc function [Security], _crypto2_cryptmemalloc, security.cryptmemalloc, wincrypt/CryptMemAlloc
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CryptMemAlloc
 - wincrypt/CryptMemAlloc
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
 - CryptMemAlloc
---

# CryptMemAlloc function


## -description

The <b>CryptMemAlloc</b> function allocates memory for a buffer. It is used by all Crypt32.lib functions that return allocated buffers.

## -parameters

### -param cbSize [in]

Number of bytes to be allocated.

## -returns

Returns a pointer to the buffer allocated. If the function fails, <b>NULL</b> is returned. When you have finished using the buffer, free the memory by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemrealloc">CryptMemRealloc</a>