---
UID: NC:ntsecpkg.SpCompleteAuthTokenFn
title: SpCompleteAuthTokenFn
author: windows-sdk-content
description: Completes an authentication token.
old-location: security\spcompleteauthtoken.htm
old-project: SecAuthN
ms.assetid: 2e20620a-457d-424c-a6b9-64b571174c98
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SpCompleteAuthToken, SpCompleteAuthToken function [Security], SpCompleteAuthTokenFn, _ssp_spcompleteauthtoken, ntsecpkg/SpCompleteAuthToken, security.spcompleteauthtoken
ms.prod: windows
ms.technology: windows-sdk
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
-	SpCompleteAuthToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpCompleteAuthTokenFn callback function


## -description


The <b>SpCompleteAuthToken</b> function completes an authentication token.

The <b>SpCompleteAuthToken</b> function is the dispatch function for the 
<a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param ContextHandle [in]

Handle of the context to complete.


### -param InputBuffer [in]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains package-specific information for the context.


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



SSP/APs must implement the <b>SpCompleteAuthToken</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpCompleteAuthToken</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a>



<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

