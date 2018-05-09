---
UID: NC:ntsecpkg.KspMakeSignatureFn
title: KspMakeSignatureFn
author: windows-driver-content
description: Generates a signature based on the specified message and security context.
old-location: security\spmakesignature.htm
old-project: SecAuthN
ms.assetid: 9db828f3-b15c-4e22-bbd8-5daa223b2be0
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: KspMakeSignatureFn, SpMakeSignature, SpMakeSignature function [Security], _ssp_spmakesignature, ntsecpkg/SpMakeSignature, security.spmakesignature
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
-	SpMakeSignature
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# KspMakeSignatureFn callback function


## -description


The <b>SpMakeSignature</b> function generates a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">signature</a> based on the specified message and <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.

The <b>SpMakeSignature</b> function is the dispatch function for the 
<a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param ContextId


### -param fQOP


### -param Message


### -param MessageSeqNo








#### - ContextHandle [in]

A handle to the security context to be used to generate the message signature.


#### - MessageBuffers [in, out]

Pointer to an array of 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures. On input, the structures contain the message to be signed. On output, the <b>SecBuffer</b> structure of type SECBUFFER_TOKEN contains the signature.


#### - MessageSequenceNumber [in]

Sequence number to assign to the message. Sequence numbers are optional and are used as protection against loss and insertion of messages. A value of zero indicates that sequence numbers are not in use.


#### - QualityOfProtection [in]

Specifies package-specific flags that indicate the quality of protection. A security package can use this parameter to support the selection of cryptographic algorithms.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists a common reason for failure and the error code that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 




## -remarks



The counterpart to the <b>SpMakeSignature</b> function is the 
<a href="https://msdn.microsoft.com/62a74a1d-c7e6-4722-af57-997a5ff553ee">SpVerifySignature</a> function, used to verify signatures at the receiving end.

SSP/APs must implement the <b>SpMakeSignature</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpMakeSignature</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a>



<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>



<a href="https://msdn.microsoft.com/62a74a1d-c7e6-4722-af57-997a5ff553ee">SpVerifySignature</a>
 

 

