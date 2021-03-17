---
UID: NC:ntsecpkg.LSA_COPY_TO_CLIENT_BUFFER
title: LSA_COPY_TO_CLIENT_BUFFER (ntsecpkg.h)
description: Copies information from a buffer in the current process into a client process's address space.
helpviewer_keywords: ["CopyToClientBuffer","CopyToClientBuffer callback function [Security]","LSA_COPY_TO_CLIENT_BUFFER","LSA_COPY_TO_CLIENT_BUFFER callback","_lsa_copytoclientbuffer","ntsecpkg/CopyToClientBuffer","security.copytoclientbuffer"]
old-location: security\copytoclientbuffer.htm
tech.root: security
ms.assetid: 53ea2c99-7934-447d-9ec5-e88ee925ca89
ms.date: 12/05/2018
ms.keywords: CopyToClientBuffer, CopyToClientBuffer callback function [Security], LSA_COPY_TO_CLIENT_BUFFER, LSA_COPY_TO_CLIENT_BUFFER callback, _lsa_copytoclientbuffer, ntsecpkg/CopyToClientBuffer, security.copytoclientbuffer
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
 - LSA_COPY_TO_CLIENT_BUFFER
 - ntsecpkg/LSA_COPY_TO_CLIENT_BUFFER
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
 - CopyToClientBuffer
---

# LSA_COPY_TO_CLIENT_BUFFER callback function


## -description

Copies information from a buffer in the current process into a client process's address space.

## -parameters

### -param ClientRequest [in]

Pointer to an opaque 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> data type representing a client request.

### -param Length [in]

Length in bytes of the buffer to be copied.

### -param ClientBaseAddress [in]

Pointer to a buffer that receives the data. This address is the address of the buffer within the client process, not the current process.

### -param BufferToCopy [in]

Pointer to the local buffer whose contents are to be copied into the client address space.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>