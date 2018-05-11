---
UID: NC:ntsecpkg.LSA_ALLOCATE_CLIENT_BUFFER
title: LSA_ALLOCATE_CLIENT_BUFFER
author: windows-driver-content
description: Allocates a buffer in the client's address space.
old-location: security\allocateclientbuffer.htm
old-project: SecAuthN
ms.assetid: 2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: AllocateClientBuffer, AllocateClientBuffer function [Security], LSA_ALLOCATE_CLIENT_BUFFER, _lsa_allocateclientbuffer, ntsecpkg/AllocateClientBuffer, security.allocateclientbuffer
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
-	AllocateClientBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_ALLOCATE_CLIENT_BUFFER callback function


## -description


Allocates a buffer in the client's address space. Buffers allocated in the client's address space are used to hold information returned to the client from an authentication package.
			
		


## -parameters




### -param ClientRequest [in]

Pointer to an opaque 
<a href="https://msdn.microsoft.com/384dd6e0-726f-4100-a036-1cca6a332a64">LSA_CLIENT_REQUEST</a> data structure that contains information about the LSA client's authentication request. A custom authentication package should pass in the value received during the client's call to the function, such as 
<a href="https://msdn.microsoft.com/be0f9886-c0f6-4361-96c7-d16da8713fc7">LsaApCallPackage</a> or 
<a href="https://msdn.microsoft.com/4c8def77-d536-486e-a830-9df3848fbccb">LsaApLogonUser</a>, that returns the output parameter.


### -param LengthRequired [in]

Length of the buffer needed, in bytes.


### -param *ClientBaseAddress [out]

Pointer that receives the address of the buffer. This address is the virtual address of the buffer within the client process, not in the current process.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

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
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



The authentication package or the client process must later free the buffer. The authentication process can free the buffer by using the 
<a href="https://msdn.microsoft.com/c3a92039-7fb1-49e9-8e7a-0c902770543e">FreeClientBuffer</a> dispatch routine. The client process can free the buffer by using the 
<a href="https://msdn.microsoft.com/e814ed68-07e7-4936-ba96-5411086f43f6">LsaFreeReturnBuffer</a> function.




## -see-also




<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

