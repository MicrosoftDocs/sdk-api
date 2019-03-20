---
UID: NC:ntsecpkg.LSA_COPY_TO_CLIENT_BUFFER
title: LSA_COPY_TO_CLIENT_BUFFER (ntsecpkg.h)
author: windows-sdk-content
description: Copies information from a buffer in the current process into a client process's address space.
old-location: security\copytoclientbuffer.htm
tech.root: SecAuthN
ms.assetid: 53ea2c99-7934-447d-9ec5-e88ee925ca89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyToClientBuffer, CopyToClientBuffer callback function [Security], LSA_COPY_TO_CLIENT_BUFFER, LSA_COPY_TO_CLIENT_BUFFER callback, _lsa_copytoclientbuffer, ntsecpkg/CopyToClientBuffer, security.copytoclientbuffer
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
 - CopyToClientBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LSA_COPY_TO_CLIENT_BUFFER callback function


## -description


Copies information from a buffer in the current process into a client process's address space.


## -parameters




### -param ClientRequest [in]

Pointer to an opaque 
<a href="https://msdn.microsoft.com/384dd6e0-726f-4100-a036-1cca6a332a64">LSA_CLIENT_REQUEST</a> data type representing a client request.


### -param Length [in]

Length in bytes of the buffer to be copied.


### -param ClientBaseAddress [in]

Pointer to a buffer that receives the data. This address is the address of the buffer within the client process, not the current process.


### -param BufferToCopy [in]

Pointer to the local buffer whose contents are to be copied into the client address space.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

