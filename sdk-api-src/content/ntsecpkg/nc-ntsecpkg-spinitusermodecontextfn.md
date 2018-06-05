---
UID: NC:ntsecpkg.SpInitUserModeContextFn
title: SpInitUserModeContextFn
author: windows-sdk-content
description: Creates a user-mode security context from a packed Local Security Authority (LSA)-mode context.
old-location: security\spinitusermodecontext.htm
old-project: SecAuthN
ms.assetid: e67a7ad3-b3d2-4c1a-a514-f51ccfaf990e
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SpInitUserModeContext, SpInitUserModeContext function [Security], SpInitUserModeContextFn, _ssp_spinitusermodecontext, ntsecpkg/SpInitUserModeContext, security.spinitusermodecontext
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
tech.root: 
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	SpInitUserModeContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpInitUserModeContextFn callback function


## -description


The <b>SpInitUserModeContext</b> function creates a user-mode <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> from a packed <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA)-mode context.


## -parameters




### -param ContextHandle [in]

A handle to the LSA-mode context returned from the 
<a href="https://msdn.microsoft.com/e733d6fb-0ce6-4fd2-a8e2-54aa44602828">SpInitLsaModeContext</a> or 
<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a> function.


### -param PackedContext [in]

Pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that contains the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">serialized</a> context data. Use the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function to free memory allocated for this structure.


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
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to create the context.

</td>
</tr>
</table>
 




## -remarks



The <b>SpInitUserModeContext</b> function is called after a security context has been created by the security package, if the <i>MappedContext</i> parameter of the 
<a href="https://msdn.microsoft.com/e733d6fb-0ce6-4fd2-a8e2-54aa44602828">SpInitLsaModeContext</a> or 
<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a> is set to <b>TRUE</b>. The package-specific context data should contain the information required to determine which function resulted in the call to <b>SpInitUserModeContext</b>.

SSP/APs must implement the <b>SpInitUserModeContext</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpInitUserModeContext</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a>



<a href="https://msdn.microsoft.com/e733d6fb-0ce6-4fd2-a8e2-54aa44602828">SpInitLsaModeContext</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

