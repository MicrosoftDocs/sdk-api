---
UID: NF:ntsecapi.LsaFreeReturnBuffer
title: LsaFreeReturnBuffer function
author: windows-sdk-content
description: Frees the memory used by a buffer previously allocated by the LSA.
old-location: security\lsafreereturnbuffer.htm
old-project: SecAuthN
ms.assetid: e814ed68-07e7-4936-ba96-5411086f43f6
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: LsaFreeReturnBuffer, LsaFreeReturnBuffer function [Security], _lsa_lsafreereturnbuffer, ntsecapi/LsaFreeReturnBuffer, security.lsafreereturnbuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaFreeReturnBuffer
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LsaFreeReturnBuffer function


## -description


The <b>LsaFreeReturnBuffer</b> function frees the memory used by a buffer previously allocated by the LSA.


## -parameters




### -param Buffer [in]

Pointer to the buffer to be freed.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



Some of the LSA authentication functions allocate memory buffers to hold returned information, for example, 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> and 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>. Your application should call <b>LsaFreeReturnBuffer</b> to free these buffers when they are no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>



<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>
 

 

