---
UID: NC:ntsecpkg.LSA_COPY_FROM_CLIENT_BUFFER
title: LSA_COPY_FROM_CLIENT_BUFFER
author: windows-driver-content
description: Copies information from the address space of a client process into a buffer in the current process.
old-location: security\copyfromclientbuffer.htm
old-project: SecAuthN
ms.assetid: d753694e-38f9-47d1-b860-252123ae6f16
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CopyFromClientBuffer, CopyFromClientBuffer function [Security], LSA_COPY_FROM_CLIENT_BUFFER, _lsa_copyfromclientbuffer, ntsecpkg/CopyFromClientBuffer, security.copyfromclientbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	CopyFromClientBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_COPY_FROM_CLIENT_BUFFER callback


## -description


Copies information from the address space of a  client process into a buffer in the current process.


## -parameters




### -param ClientRequest [in]

Pointer to an opaque 
<a href="https://msdn.microsoft.com/384dd6e0-726f-4100-a036-1cca6a332a64">LSA_CLIENT_REQUEST</a> data structure that contains information about the LSA client's authentication request.


### -param Length [in]

Length of the buffer to be copied, in bytes.


### -param BufferToCopy [in]

Pointer to the local buffer into which the data is to be copied.


### -param ClientBaseAddress [in]

Pointer to the client buffer whose contents are to be copied. This address is the address of the buffer within the client process, not the current process.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

