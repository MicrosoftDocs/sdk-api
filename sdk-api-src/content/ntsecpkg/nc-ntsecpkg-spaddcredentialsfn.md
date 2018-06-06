---
UID: NC:ntsecpkg.SpAddCredentialsFn
title: SpAddCredentialsFn
author: windows-sdk-content
description: Used to add credentials for a security principal.
old-location: security\spaddcredentials.htm
old-project: SecAuthN
ms.assetid: 27377afa-4e54-4c6b-8e84-a8810bc01139
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SECPKG_CRED_INBOUND, SECPKG_CRED_OUTBOUND, SpAddCredentials, SpAddCredentials function [Security], SpAddCredentialsFn, _ssp_spaddcredentials, ntsecpkg/SpAddCredentials, security.spaddcredentials
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
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpAddCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpAddCredentialsFn callback function


## -description


Used to add <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> for a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a>.


## -parameters




### -param CredentialHandle [in]

A handle to the credential to add.


### -param PrincipalName [in]

Optional. Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure containing the name of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a> whose credentials are being added.


### -param Package [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure containing the name of the authenticating package.


### -param CredentialUseFlags [in]

Flags indicating how the credentials will be used. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_INBOUND"></a><a id="secpkg_cred_inbound"></a><dl>
<dt><b>SECPKG_CRED_INBOUND</b></dt>
</dl>
</td>
<td width="60%">
Credentials will be used with the 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_OUTBOUND"></a><a id="secpkg_cred_outbound"></a><dl>
<dt><b>SECPKG_CRED_OUTBOUND</b></dt>
</dl>
</td>
<td width="60%">
Credentials will be used with the 
<a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> function.

</td>
</tr>
</table>
 


### -param AuthorizationData [in]

Optional. Pointer to supplemental authentication data.


### -param GetKeyFunciton


### -param GetKeyArgument [in]

Pointer to the argument used with the <i>GetKeyFunction</i> function.
					


### -param ExpirationTime [out]

Pointer to a 
<a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a> that receives the time the credentials handle expires.


#### - GetKeyFunction [in]

Pointer to a function in the caller's address space that generates <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session keys</a>.


## -returns




						If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



SSP/APs must implement the <b>SpAddCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpAddCredentials</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

