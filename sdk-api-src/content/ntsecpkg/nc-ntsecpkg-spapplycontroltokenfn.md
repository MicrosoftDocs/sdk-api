---
UID: NC:ntsecpkg.SpApplyControlTokenFn
title: SpApplyControlTokenFn
author: windows-sdk-content
description: Applies a control token to a security context. This function is not currently called by the Local Security Authority (LSA).
old-location: security\spapplycontroltoken.htm
tech.root: SecAuthN
ms.assetid: 60c5e310-dd80-4bf7-9480-ac614c98d75f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SpApplyControlToken, SpApplyControlToken callback function [Security], SpApplyControlTokenFn, SpApplyControlTokenFn callback, _ssp_spapplycontroltoken, ntsecpkg/SpApplyControlToken, security.spapplycontroltoken
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
 - SpApplyControlToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SpApplyControlTokenFn callback function


## -description


Applies a control token to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. This function is not currently called by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA).


## -parameters




### -param ContextHandle [in]

A handle to the security context to be modified based on the <i>ControlToken</i> parameter.


### -param ControlToken [in]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure containing the token to apply to the context.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists common reasons for failure and the error codes that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
The token is not valid.

</td>
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



SSP/APs must implement the <b>SpApplyControlToken</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpApplyControlToken</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

