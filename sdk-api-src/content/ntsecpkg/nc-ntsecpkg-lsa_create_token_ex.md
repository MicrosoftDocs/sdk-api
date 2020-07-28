---
UID: NC:ntsecpkg.LSA_CREATE_TOKEN_EX
title: LSA_CREATE_TOKEN_EX (ntsecpkg.h)
description: Creates tokens while processing calls to SpAcceptLsaModeContext.
helpviewer_keywords: ["CreateTokenEx","CreateTokenEx callback function [Security]","LSA_CREATE_TOKEN_EX","LSA_CREATE_TOKEN_EX callback","LsaTokenInformationNull","LsaTokenInformationV1","ntsecpkg/CreateTokenEx","security.createtokenex"]
old-location: security\createtokenex.htm
tech.root: security
ms.assetid: 1f12d8a4-6cbd-43e3-98a7-eaf3d30a053e
ms.date: 12/05/2018
ms.keywords: CreateTokenEx, CreateTokenEx callback function [Security], LSA_CREATE_TOKEN_EX, LSA_CREATE_TOKEN_EX callback, LsaTokenInformationNull, LsaTokenInformationV1, ntsecpkg/CreateTokenEx, security.createtokenex
f1_keywords:
- ntsecpkg/CreateTokenEx
dev_langs:
- c++
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
- CreateTokenEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_CREATE_TOKEN_EX callback function


## -description


Creates tokens while processing calls to 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn">SpAcceptLsaModeContext</a>.


## -parameters




### -param LogonId [in]

A pointer to a logon session identifier for the new token. This identifier is obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_logon_session">CreateLogonSession</a>.


### -param TokenSource [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a> structure that specifies the source for this token. Specify the package name.


### -param LogonType [in]

A 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a> value that indicates the type of logon.


### -param ImpersonationLevel [in]

A 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> value that indicates the extent to which a server process can impersonate a client process.


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

<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_token_information_null">LSA_TOKEN_INFORMATION_NULL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LsaTokenInformationV1"></a><a id="lsatokeninformationv1"></a><a id="LSATOKENINFORMATIONV1"></a><dl>
<dt><b>LsaTokenInformationV1</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa378721(v=vs.85)">LSA_TOKEN_INFORMATION_V1</a>


</td>
</tr>
</table>
 


### -param TokenInformation [in]

A pointer to the token information. The type of structure pointed to by <i>TokenInformation</i> is indicated by the <i>TokenInformationType</i> parameter.


### -param TokenGroups [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that specifies groups not contained in <i>TokenInformation</i>.


### -param Workstation [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the name of the client's workstation, normally a NetBIOS name.


### -param ProfilePath [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the path to the user's profile, if any.


### -param SessionInformation [in]

Data that specifies information about the current logon session. The format of this data is specified by the value of the <i>SessionInformationType</i> parameter.


### -param SessionInformationType [in]

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ne-ntsecpkg-secpkg_sessioninfo_type">SECPKG_SESSIONINFO_TYPE</a> enumeration that specifies the format of the <i>SessionInformation</i> parameter. Currently, the only defined value is <b>SecSessionPrimaryCred</b>, which specifies that the value of the <i>SessionInformation</i> parameter is a <a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_primary_cred">SECPKG_PRIMARY_CRED</a> structure.


### -param Token [out]

A pointer that receives the address of a handle to the new token. When you have finished using the handle, close it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.


### -param SubStatus [out]

A pointer to a variable that receives error information.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.
						

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.




## -remarks



A pointer to the <b>CreateTokenEx</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
 

 

