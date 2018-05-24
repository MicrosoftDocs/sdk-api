---
UID: NC:ntsecpkg.LSA_CREATE_TOKEN
title: LSA_CREATE_TOKEN
author: windows-driver-content
description: The CreateToken function is used by SSP/APs to create tokens while processing calls to SpAcceptLsaModeContext.
old-location: security\createtoken.htm
old-project: SecAuthN
ms.assetid: 2355cf1d-9f95-40be-aed4-8c2796137960
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CreateToken, CreateToken function [Security], LSA_CREATE_TOKEN, LsaTokenInformationNull, LsaTokenInformationV1, _ssp_createtoken, ntsecpkg/CreateToken, security.createtoken
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
-	CreateToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_CREATE_TOKEN callback function


## -description



			The <b>CreateToken</b> function is used by SSP/APs to create tokens while processing calls to 
<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a>.


## -parameters




### -param LogonId [in]

Pointer to a logon session identifier for the new token. This identifier is obtained from a previous call to 
<a href="https://msdn.microsoft.com/383c935c-a1f2-4d1b-bb02-e7e37f154771">CreateLogonSession</a>.


### -param TokenSource [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a> structure that specifies the source for this token. Specify the package name.


### -param LogonType [in]

A 
<a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a> value that indicates the type of logon.


### -param ImpersonationLevel [in]

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a> value that indicates the extent to which a server process can impersonate a client process.


### -param TokenInformationType [in]

Specifies the type of structure in the <i>TokenInformation</i> parameter. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LsaTokenInformationNull"></a><a id="lsatokeninformationnull"></a><a id="LSATOKENINFORMATIONNULL"></a><dl>
<dt><b>LsaTokenInformationNull</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/fbcd0f78-1ad5-4bea-a95f-d19fb3894537">LSA_TOKEN_INFORMATION_NULL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LsaTokenInformationV1"></a><a id="lsatokeninformationv1"></a><a id="LSATOKENINFORMATIONV1"></a><dl>
<dt><b>LsaTokenInformationV1</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/e4c43828-aa5c-443c-93ad-96bb986533c5">LSA_TOKEN_INFORMATION_V1</a>


</td>
</tr>
</table>
 


### -param TokenInformation [in]

Pointer to the token information. The type of structure pointed to by <i>TokenInformation</i> is indicated by the <i>TokenInformationType</i> parameter.

If the structure pointed to by this parameter is an <a href="https://msdn.microsoft.com/e4c43828-aa5c-443c-93ad-96bb986533c5">LSA_TOKEN_INFORMATION_V1</a> structure, the caller must allocate the memory for the <b>Groups</b> member of that structure by calling the <a href="https://msdn.microsoft.com/956e7aaf-e8b3-4db5-945a-b579f946b769">AllocatePrivateHeap</a> function.


### -param TokenGroups [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that specifies groups not contained in <i>TokenInformation</i>.


### -param AccountName [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that contains the name of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a>. This information is used for auditing and name searches.


### -param AuthorityName [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that contains the name of the authority that validated the logon <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a>, normally the Windows domain name.


### -param Workstation [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that contains the name of the client's workstation, normally a NetBIOS name.


### -param ProfilePath [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that contains the path to the user's profile, if any.


### -param Token [out]

Pointer that receives the address of a handle to the new token. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


### -param SubStatus [out]

Pointer to a variable that receives error information.


## -returns




						If the function succeeds, the return value is STATUS_SUCCESS.
						

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.




## -remarks



A pointer to the <b>CreateToken</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

