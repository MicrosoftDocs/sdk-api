---
UID: NC:ntsecpkg.LSA_CONVERT_AUTH_DATA_TO_TOKEN
title: LSA_CONVERT_AUTH_DATA_TO_TOKEN (ntsecpkg.h)
description: The ConvertAuthDataToToken function creates an access token from the authorization data returned from the GetAuthDataForUser or GetUserAuthData functions.
helpviewer_keywords: ["ConvertAuthDataToToken","ConvertAuthDataToToken callback function [Security]","LSA_CONVERT_AUTH_DATA_TO_TOKEN","LSA_CONVERT_AUTH_DATA_TO_TOKEN callback","_ssp_convertauthdatatotoken","ntsecpkg/ConvertAuthDataToToken","security.convertauthdatatotoken"]
old-location: security\convertauthdatatotoken.htm
tech.root: security
ms.assetid: 99dfd3b3-40e0-44b2-8752-39b7b394ac0e
ms.date: 12/05/2018
ms.keywords: ConvertAuthDataToToken, ConvertAuthDataToToken callback function [Security], LSA_CONVERT_AUTH_DATA_TO_TOKEN, LSA_CONVERT_AUTH_DATA_TO_TOKEN callback, _ssp_convertauthdatatotoken, ntsecpkg/ConvertAuthDataToToken, security.convertauthdatatotoken
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
 - LSA_CONVERT_AUTH_DATA_TO_TOKEN
 - ntsecpkg/LSA_CONVERT_AUTH_DATA_TO_TOKEN
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
 - ConvertAuthDataToToken
---

# LSA_CONVERT_AUTH_DATA_TO_TOKEN callback function


## -description

The <b>ConvertAuthDataToToken</b> function creates an access token from the authorization data returned from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_auth_data_for_user">GetAuthDataForUser</a> or 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_user_auth_data">GetUserAuthData</a> functions.

## -parameters

### -param UserAuthData [in]

Pointer to the authorization data received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_auth_data_for_user">GetAuthDataForUser</a> or 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_user_auth_data">GetUserAuthData</a> functions.

### -param UserAuthDataSize [in]

Size, in bytes, of the authorization data specified by the <i>UserAuthData</i> parameter.

### -param ImpersonationLevel [in]

A 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> value specifying the impersonation level for the token to be created.

### -param TokenSource [in]

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a> structure specifying the source to record in the token.

### -param LogonType [in]

A 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a> value indicating the type of logon to record in the token.

### -param AuthorityName [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that specifies the name of the authority that authorized this user, typically a domain name.

### -param Token [out]

Pointer to a HANDLE that receives the user token handle.

When you have finished using the user token, release the handle by calling <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

### -param LogonId [out]

Pointer to an <a href="/windows/desktop/SecGloss/l-gly">LUID</a> that receives the <a href="/windows/desktop/SecGloss/l-gly">logon identifier</a> for the token.

### -param AccountName [out]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that receives the account name encoded in the <i>UserAuthData</i> parameter.

### -param SubStatus [out]

Pointer to a variable that receives additional information about the return value of the function call.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.

## -remarks

A pointer to the <b>ConvertAuthDataToToken</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_auth_data_for_user">GetAuthDataForUser</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_user_auth_data">GetUserAuthData</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-security_logon_type">SECURITY_LOGON_TYPE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a>