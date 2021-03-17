---
UID: NC:ntsecpkg.LSA_PROTECT_MEMORY
title: LSA_PROTECT_MEMORY (ntsecpkg.h)
description: Encrypts the specified memory buffer.
helpviewer_keywords: ["LSA_PROTECT_MEMORY","LSA_PROTECT_MEMORY callback","LsaProtectMemory","LsaProtectMemory callback function [Security]","ntsecpkg/LsaProtectMemory","security.lsaprotectmemory"]
old-location: security\lsaprotectmemory.htm
tech.root: security
ms.assetid: c851fe8b-be22-4966-ab99-f177989cf382
ms.date: 12/05/2018
ms.keywords: LSA_PROTECT_MEMORY, LSA_PROTECT_MEMORY callback, LsaProtectMemory, LsaProtectMemory callback function [Security], ntsecpkg/LsaProtectMemory, security.lsaprotectmemory
req.header: ntsecpkg.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_PROTECT_MEMORY
 - ntsecpkg/LSA_PROTECT_MEMORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - LsaProtectMemory
---

# LSA_PROTECT_MEMORY callback function


## -description

Encrypts the specified memory buffer.

## -parameters

### -param Buffer [in, out]

On input, a pointer to the buffer to be encrypted. On output, a pointer to the encrypted buffer.

### -param BufferSize [in]

The size, in bytes, of the <i>Buffer</i> buffer.

## -remarks

A pointer to the <b>LsaProtectMemory</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>