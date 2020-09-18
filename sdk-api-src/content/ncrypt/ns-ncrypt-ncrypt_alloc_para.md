---
UID: NS:ncrypt.NCRYPT_ALLOC_PARA
title: NCRYPT_ALLOC_PARA (ncrypt.h)
description: Enables you to specify custom functions that can be used to allocate and free data.
helpviewer_keywords: ["NCRYPT_ALLOC_PARA","NCRYPT_ALLOC_PARA structure [Security]","PNCRYPT_ALLOC_PARA","PNCRYPT_ALLOC_PARA structure pointer [Security]","ncrypt/NCRYPT_ALLOC_PARA","ncrypt/PNCRYPT_ALLOC_PARA","security.ncrypt_alloc_para"]
old-location: security\ncrypt_alloc_para.htm
tech.root: security
ms.assetid: 4F546F51-E4DE-4703-B1D1-F84165C3C31B
ms.date: 12/05/2018
ms.keywords: NCRYPT_ALLOC_PARA, NCRYPT_ALLOC_PARA structure [Security], PNCRYPT_ALLOC_PARA, PNCRYPT_ALLOC_PARA structure pointer [Security], ncrypt/NCRYPT_ALLOC_PARA, ncrypt/PNCRYPT_ALLOC_PARA, security.ncrypt_alloc_para
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NCRYPT_ALLOC_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCRYPT_ALLOC_PARA
 - ncrypt/NCRYPT_ALLOC_PARA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ncrypt.h
api_name:
 - NCRYPT_ALLOC_PARA
---

# NCRYPT_ALLOC_PARA structure


## -description

The <b>NCRYPT_ALLOC_PARA</b> structure enables you to specify custom functions that can be used to allocate and free data. This structure is used in the following functions:
<ul>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptgetprotectiondescriptorinfo">NCryptGetProtectionDescriptorInfo</a>
</li>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptprotectsecret">NCryptProtectSecret</a>
</li>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptunprotectsecret">NCryptUnprotectSecret</a>
</li>
</ul>

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pfnAlloc

Address of a custom function that can allocate memory.

### -field pfnFree

Address of a function that can free memory allocated by the function specified by the <b>pfnAlloc</b> member.

## -see-also

<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptgetprotectiondescriptorinfo">NCryptGetProtectionDescriptorInfo</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptprotectsecret">NCryptProtectSecret</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptunprotectsecret">NCryptUnprotectSecret</a>