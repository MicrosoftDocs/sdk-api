---
UID: NC:ntsecpkg.LSA_COPY_FROM_CLIENT_BUFFER
title: LSA_COPY_FROM_CLIENT_BUFFER (ntsecpkg.h)
description: Copies information from the address space of a client process into a buffer in the current process.
helpviewer_keywords: ["CopyFromClientBuffer","CopyFromClientBuffer callback function [Security]","LSA_COPY_FROM_CLIENT_BUFFER","LSA_COPY_FROM_CLIENT_BUFFER callback","_lsa_copyfromclientbuffer","ntsecpkg/CopyFromClientBuffer","security.copyfromclientbuffer"]
old-location: security\copyfromclientbuffer.htm
tech.root: security
ms.assetid: d753694e-38f9-47d1-b860-252123ae6f16
ms.date: 12/05/2018
ms.keywords: CopyFromClientBuffer, CopyFromClientBuffer callback function [Security], LSA_COPY_FROM_CLIENT_BUFFER, LSA_COPY_FROM_CLIENT_BUFFER callback, _lsa_copyfromclientbuffer, ntsecpkg/CopyFromClientBuffer, security.copyfromclientbuffer
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
 - LSA_COPY_FROM_CLIENT_BUFFER
 - ntsecpkg/LSA_COPY_FROM_CLIENT_BUFFER
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
 - CopyFromClientBuffer
---

# LSA_COPY_FROM_CLIENT_BUFFER callback function


## -description

Copies information from the address space of a  client process into a buffer in the current process.

## -parameters

### -param ClientRequest [in]

Pointer to an opaque 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> data structure that contains information about the LSA client's authentication request.

### -param Length [in]

Length of the buffer to be copied, in bytes.

### -param BufferToCopy [in]

Pointer to the local buffer into which the data is to be copied.

### -param ClientBaseAddress [in]

Pointer to the client buffer whose contents are to be copied. This address is the address of the buffer within the client process, not the current process.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>