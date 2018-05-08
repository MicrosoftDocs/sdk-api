---
UID: NC:ntsecpkg.SpGetContextTokenFn
title: SpGetContextTokenFn
author: windows-driver-content
description: Obtains the token to impersonate.
old-location: security\spgetcontexttoken.htm
old-project: SecAuthN
ms.assetid: d2e6b57d-751d-4f07-b05b-6d3aabd60650
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SpGetContextToken, SpGetContextToken function [Security], SpGetContextTokenFn, _ssp_spgetcontexttoken, ntsecpkg/SpGetContextToken, security.spgetcontexttoken
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
-	SpGetContextToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SpGetContextTokenFn callback function


## -description


Obtains the token to impersonate. The <b>SpGetContextToken</b> function is used by the SSPI 
<a href="https://msdn.microsoft.com/167eaf3b-b794-4587-946d-fa596f1f9411">ImpersonateSecurityContext</a> function to obtain the token to impersonate.


## -parameters




### -param ContextHandle [in]

A handle to the context to impersonate.


### -param ImpersonationToken [out]

Pointer that receives a handle to the token for the specified context. Return the handle to the token without first duplicating the handle or the token.


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



SSP/APs must implement the <b>SpGetContextToken</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetContextToken</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/167eaf3b-b794-4587-946d-fa596f1f9411">ImpersonateSecurityContext</a>



<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

