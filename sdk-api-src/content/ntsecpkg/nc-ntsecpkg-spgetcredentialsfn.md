---
UID: NC:ntsecpkg.SpGetCredentialsFn
title: SpGetCredentialsFn
author: windows-driver-content
description: Retrieves the primary and supplemental credentials from the user object.
old-location: security\spgetcredentials.htm
old-project: SecAuthN
ms.assetid: bdf96b19-30eb-4cb2-b3ec-bd6f406233c5
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: SpGetCredentials, SpGetCredentials function [Security], SpGetCredentialsFn, _ssp_spgetcredentials, ntsecpkg/SpGetCredentials, security.spgetcredentials
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
-	SpGetCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SpGetCredentialsFn callback function


## -description


The <b>SpGetCredentials</b> function retrieves the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary</a> and <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a> from the user object.


## -parameters




### -param CredentialHandle [in]

A handle to the credentials to be retrieved.


### -param Credentials [out]

Pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives the credentials.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code indicating the reason it failed. The following  lists common reasons for failure and the error codes that the function should return. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not sufficient memory to retrieve the credentials.

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



SSP/APs must implement the <b>SpGetCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetCredentials</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

