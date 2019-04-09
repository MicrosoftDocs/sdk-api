---
UID: NC:ntsecpkg.LSA_FREE_CLIENT_BUFFER
title: LSA_FREE_CLIENT_BUFFER (ntsecpkg.h)
author: windows-sdk-content
description: Frees a client buffer previously allocated with the AllocateClientBuffer function.
old-location: security\freeclientbuffer.htm
tech.root: SecAuthN
ms.assetid: c3a92039-7fb1-49e9-8e7a-0c902770543e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeClientBuffer, FreeClientBuffer callback function [Security], LSA_FREE_CLIENT_BUFFER, LSA_FREE_CLIENT_BUFFER callback, _lsa_freeclientbuffer, ntsecpkg/FreeClientBuffer, security.freeclientbuffer
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - FreeClientBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LSA_FREE_CLIENT_BUFFER callback function


## -description


Frees a client buffer previously allocated with the 
<a href="https://msdn.microsoft.com/2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe">AllocateClientBuffer</a> function.


## -parameters




### -param ClientRequest [in]

Pointer to an opaque 
<a href="https://msdn.microsoft.com/384dd6e0-726f-4100-a036-1cca6a332a64">LSA_CLIENT_REQUEST</a> data type containing information about the LSA client's request.


### -param ClientBaseAddress [in]

Optional. Pointer to the buffer to be freed. This address is the virtual address of the buffer within the client process, not in the current process. If <b>NULL</b> is passed, no memory is freed. This allows the client to pass in a value returned to it by the LSA without knowing whether the LSA actually allocated a buffer.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



Because this function frees pages in the client's process, it must be called with great care. Calling this function with an address that is not valid can cause the client process to crash.




## -see-also




<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

