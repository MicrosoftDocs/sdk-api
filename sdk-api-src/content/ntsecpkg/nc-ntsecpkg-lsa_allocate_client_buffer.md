---
UID: NC:ntsecpkg.LSA_ALLOCATE_CLIENT_BUFFER
title: LSA_ALLOCATE_CLIENT_BUFFER (ntsecpkg.h)
description: Allocates a buffer in the client's address space.
helpviewer_keywords: ["AllocateClientBuffer","AllocateClientBuffer callback function [Security]","LSA_ALLOCATE_CLIENT_BUFFER","LSA_ALLOCATE_CLIENT_BUFFER callback","_lsa_allocateclientbuffer","ntsecpkg/AllocateClientBuffer","security.allocateclientbuffer"]
old-location: security\allocateclientbuffer.htm
tech.root: security
ms.assetid: 2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe
ms.date: 12/05/2018
ms.keywords: AllocateClientBuffer, AllocateClientBuffer callback function [Security], LSA_ALLOCATE_CLIENT_BUFFER, LSA_ALLOCATE_CLIENT_BUFFER callback, _lsa_allocateclientbuffer, ntsecpkg/AllocateClientBuffer, security.allocateclientbuffer
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
 - LSA_ALLOCATE_CLIENT_BUFFER
 - ntsecpkg/LSA_ALLOCATE_CLIENT_BUFFER
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
 - AllocateClientBuffer
---

# LSA_ALLOCATE_CLIENT_BUFFER callback function


## -description

Allocates a buffer in the client's address space. Buffers allocated in the client's address space are used to hold information returned to the client from an authentication package.

## -parameters

### -param ClientRequest [in]

Pointer to an opaque 
<a href="/windows/desktop/SecAuthN/plsa-client-request">LSA_CLIENT_REQUEST</a> data structure that contains information about the LSA client's authentication request. A custom authentication package should pass in the value received during the client's call to the function, such as 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_call_package">LsaApCallPackage</a> or 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a>, that returns the output parameter.

### -param LengthRequired [in]

Length of the buffer needed, in bytes.

### -param ClientBaseAddress [out]

Pointer that receives the address of the buffer. This address is the virtual address of the buffer within the client process, not in the current process.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The client process does not have an adequate memory quota to allocate the buffer.

</td>
</tr>
</table>
 

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

The authentication package or the client process must later free the buffer. The authentication process can free the buffer by using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_client_buffer">FreeClientBuffer</a> dispatch routine. The client process can free the buffer by using the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreereturnbuffer">LsaFreeReturnBuffer</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>
