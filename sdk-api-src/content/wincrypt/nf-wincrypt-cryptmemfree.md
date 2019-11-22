---
UID: NF:wincrypt.CryptMemFree
title: CryptMemFree function (wincrypt.h)

description: The CryptMemFree function frees memory allocated by CryptMemAlloc or CryptMemRealloc.
old-location: security\cryptmemfree.htm
tech.root: SecCrypto
ms.assetid: fb5c10ba-da8e-4a34-9302-67586a0a9624

ms.date: 12/05/2018
ms.keywords: CryptMemFree, CryptMemFree function [Security], _crypto2_cryptmemfree, security.cryptmemfree, wincrypt/CryptMemFree
ms.topic: function
f1_keywords: 
 - "wincrypt/CryptMemFree"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptMemFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptMemFree function


## -description


The <b>CryptMemFree</b> function frees memory allocated by 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemalloc">CryptMemAlloc</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemrealloc">CryptMemRealloc</a>.


## -parameters




### -param pv [in]

A pointer to the buffer to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemalloc">CryptMemAlloc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemrealloc">CryptMemRealloc</a>
 

 

