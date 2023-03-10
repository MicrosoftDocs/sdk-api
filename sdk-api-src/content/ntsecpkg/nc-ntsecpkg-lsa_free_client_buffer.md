---
UID: NC:ntsecpkg.LSA_FREE_CLIENT_BUFFER
title: LSA_FREE_CLIENT_BUFFER (ntsecpkg.h)
description: Frees a client buffer previously allocated with the AllocateClientBuffer function.
helpviewer_keywords: ["FreeClientBuffer","FreeClientBuffer callback function [Security]","LSA_FREE_CLIENT_BUFFER","LSA_FREE_CLIENT_BUFFER callback","_lsa_freeclientbuffer","ntsecpkg/FreeClientBuffer","security.freeclientbuffer"]
old-location: security\freeclientbuffer.htm
tech.root: security
ms.assetid: c3a92039-7fb1-49e9-8e7a-0c902770543e
ms.date: 12/05/2018
ms.keywords: FreeClientBuffer, FreeClientBuffer callback function [Security], LSA_FREE_CLIENT_BUFFER, LSA_FREE_CLIENT_BUFFER callback, _lsa_freeclientbuffer, ntsecpkg/FreeClientBuffer, security.freeclientbuffer
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
 - LSA_FREE_CLIENT_BUFFER
 - ntsecpkg/LSA_FREE_CLIENT_BUFFER
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
 - FreeClientBuffer
---

# LSA_FREE_CLIENT_BUFFER callback function


## -description

Frees a client buffer previously allocated with the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function.

## -parameters

### -param ClientRequest [in]

Pointer to an opaque 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> data type containing information about the LSA client's request.

### -param ClientBaseAddress [in]

Optional. Pointer to the buffer to be freed. This address is the virtual address of the buffer within the client process, not in the current process. If <b>NULL</b> is passed, no memory is freed. This allows the client to pass in a value returned to it by the LSA without knowing whether the LSA actually allocated a buffer.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

Because this function frees pages in the client's process, it must be called with great care. Calling this function with an address that is not valid can cause the client process to crash.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>