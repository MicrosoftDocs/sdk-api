---
UID: NC:ntsecpkg.LSA_CREATE_TOKEN
title: LSA_CREATE_TOKEN (ntsecpkg.h)
description: The CreateToken function is used by SSP/APs to create tokens while processing calls to SpAcceptLsaModeContext.
helpviewer_keywords: ["CreateToken","CreateToken callback function [Security]","LSA_CREATE_TOKEN","LSA_CREATE_TOKEN callback","LsaTokenInformationNull","LsaTokenInformationV1","_ssp_createtoken","ntsecpkg/CreateToken","security.createtoken"]
old-location: security\createtoken.htm
tech.root: security
ms.assetid: 2355cf1d-9f95-40be-aed4-8c2796137960
ms.date: 12/05/2018
ms.keywords: CreateToken, CreateToken callback function [Security], LSA_CREATE_TOKEN, LSA_CREATE_TOKEN callback, LsaTokenInformationNull, LsaTokenInformationV1, _ssp_createtoken, ntsecpkg/CreateToken, security.createtoken
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_CREATE_TOKEN
 - ntsecpkg/LSA_CREATE_TOKEN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - CreateToken
---

# LSA_CREATE_TOKEN callback function


## -description

The <b>CreateToken</b> function is used by SSP/APs to create tokens while processing calls to 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn">SpAcceptLsaModeContext</a>.

## -parameters

### -param LogonId [in]

Pointer to a logon session identifier for the new token. This identifier is obtained from a previous call to 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_logon_session">CreateLogonSession</a>.

### -param TokenSource [in]

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a> structure that specifies the source for this token. Specify the package name.

### -param LogonType [in]

A 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a> value that indicates the type of logon.

### -param ImpersonationLevel [in]

A 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> value that indicates the extent to which a server process can impersonate a client process.

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

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_token_information_null">LSA_TOKEN_INFORMATION_NULL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LsaTokenInformationV1"></a><a id="lsatokeninformationv1"></a><a id="LSATOKENINFORMATIONV1"></a><dl>
<dt><b>LsaTokenInformationV1</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/aa378721(v=vs.85)">LSA_TOKEN_INFORMATION_V1</a>


</td>
</tr>
</table>

### -param TokenInformation [in]

Pointer to the token information. The type of structure pointed to by <i>TokenInformation</i> is indicated by the <i>TokenInformationType</i> parameter.

If the structure pointed to by this parameter is an <a href="/previous-versions/windows/desktop/legacy/aa378721(v=vs.85)">LSA_TOKEN_INFORMATION_V1</a> structure, the caller must allocate the memory for the <b>Groups</b> member of that structure by calling the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_private_heap">AllocatePrivateHeap</a> function.

### -param TokenGroups [in]

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that specifies groups not contained in <i>TokenInformation</i>.

### -param AccountName [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the name of the <a href="/windows/desktop/SecGloss/s-gly">security principal</a>. This information is used for auditing and name searches.

### -param AuthorityName [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the name of the authority that validated the logon <a href="/windows/desktop/SecGloss/c-gly">credentials</a>, normally the Windows domain name.

### -param Workstation [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the name of the client's workstation, normally a NetBIOS name.

### -param ProfilePath [in]

Pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the path to the user's profile, if any.

### -param Token [out]

Pointer that receives the address of a handle to the new token. When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

### -param SubStatus [out]

Pointer to a variable that receives error information.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.
						

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.

## -remarks

A pointer to the <b>CreateToken</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn">SpAcceptLsaModeContext</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>