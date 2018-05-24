---
UID: NC:ntsecpkg.LSA_CREATE_TOKEN_EX
title: LSA_CREATE_TOKEN_EX
author: windows-driver-content
description: Creates tokens while processing calls to SpAcceptLsaModeContext.
old-location: security\createtokenex.htm
old-project: SecAuthN
ms.assetid: 1f12d8a4-6cbd-43e3-98a7-eaf3d30a053e
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CreateTokenEx, CreateTokenEx function [Security], LSA_CREATE_TOKEN_EX, LsaTokenInformationNull, LsaTokenInformationV1, ntsecpkg/CreateTokenEx, security.createtokenex
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
-	CreateTokenEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_CREATE_TOKEN_EX callback function


## -description


Creates tokens while processing calls to 
<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a>.


## -parameters




### -param LogonId [in]

A pointer to a logon session identifier for the new token. This identifier is obtained from a previous call to 
<a href="https://msdn.microsoft.com/383c935c-a1f2-4d1b-bb02-e7e37f154771">CreateLogonSession</a>.


### -param TokenSource [in]

A pointer to a 
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

A pointer to the token information. The type of structure pointed to by <i>TokenInformation</i> is indicated by the <i>TokenInformationType</i> parameter.


### -param TokenGroups [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that specifies groups not contained in <i>TokenInformation</i>.


### -param Workstation [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that contains the name of the client's workstation, normally a NetBIOS name.


### -param ProfilePath [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that contains the path to the user's profile, if any.


### -param SessionInformation [in]

Data that specifies information about the current logon session. The format of this data is specified by the value of the <i>SessionInformationType</i> parameter.


### -param SessionInformationType [in]

A value of the <a href="https://msdn.microsoft.com/462b028a-9f74-4367-b89b-97fd9be301ed">SECPKG_SESSIONINFO_TYPE</a> enumeration that specifies the format of the <i>SessionInformation</i> parameter. Currently, the only defined value is <b>SecSessionPrimaryCred</b>, which specifies that the value of the <i>SessionInformation</i> parameter is a <a href="https://msdn.microsoft.com/e51fd400-6c3c-4861-ab5c-6c1800b12d31">SECPKG_PRIMARY_CRED</a> structure.


### -param Token [out]

A pointer that receives the address of a handle to the new token. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


### -param SubStatus [out]

A pointer to a variable that receives error information.


## -returns




						If the function succeeds, the return value is STATUS_SUCCESS.
						

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.




## -remarks



A pointer to the <b>CreateTokenEx</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

