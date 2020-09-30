---
UID: NF:wincrypt.CryptMemRealloc
title: CryptMemRealloc function (wincrypt.h)
description: The CryptMemRealloc function frees the memory currently allocated for a buffer and allocates memory for a new buffer.
helpviewer_keywords: ["CryptMemRealloc","CryptMemRealloc function [Security]","_crypto2_cryptmemrealloc","security.cryptmemrealloc","wincrypt/CryptMemRealloc"]
old-location: security\cryptmemrealloc.htm
tech.root: security
ms.assetid: 74bdd2dd-9f05-4d36-8323-79d547820068
ms.date: 12/05/2018
ms.keywords: CryptMemRealloc, CryptMemRealloc function [Security], _crypto2_cryptmemrealloc, security.cryptmemrealloc, wincrypt/CryptMemRealloc
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
 - CryptMemRealloc
 - wincrypt/CryptMemRealloc
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
 - CryptMemRealloc
---

# CryptMemRealloc function


## -description

The <b>CryptMemRealloc</b> function frees the memory currently allocated for a buffer and allocates memory for a new buffer.

## -parameters

### -param pv [in]

A pointer to a currently allocated buffer.

### -param cbSize [in]

Number of bytes to be allocated.

## -returns

Returns a pointer to the buffer allocated. If the function fails, <b>NULL</b> is returned. When you have finished using the buffer, free the memory by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemalloc">CryptMemAlloc</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a>