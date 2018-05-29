---
UID: NC:ntsecpkg.SpFormatCredentialsFn
title: SpFormatCredentialsFn
author: windows-sdk-content
description: Formats credentials to be stored in a user object.
old-location: security\spformatcredentials.htm
old-project: SecAuthN
ms.assetid: c6036636-7f22-4f64-b507-59212d37638b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SpFormatCredentials, SpFormatCredentials function [Security], SpFormatCredentialsFn, _ssp_spformatcredentials, ntsecpkg/SpFormatCredentials, security.spformatcredentials
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
-	SpFormatCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpFormatCredentialsFn callback function


## -description


Formats <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> to be stored in a user object.


## -parameters




### -param Credentials [in]

Pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure containing the credentials to be formatted.


### -param FormattedCredentials [out]

Pointer to a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure containing the formatted credentials. Allocate memory for the structure using the 
<a href="https://msdn.microsoft.com/8e97ea0e-42f5-4641-83d7-3858c533479c">AllocateHeap</a> function.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



SSP/APs must implement the <b>SpFormatCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpFormatCredentials</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateHeap</a>



<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

