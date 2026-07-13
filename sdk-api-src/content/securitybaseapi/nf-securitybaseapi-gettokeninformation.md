---
UID: NF:securitybaseapi.GetTokenInformation
title: GetTokenInformation function (securitybaseapi.h)
description: Retrieves a specified type of information about an access token. The calling process must have appropriate access rights to obtain the information.
helpviewer_keywords: ["GetTokenInformation","GetTokenInformation function [Security]","_win32_gettokeninformation","security.gettokeninformation","securitybaseapi/GetTokenInformation"]
old-location: security\gettokeninformation.htm
tech.root: security
ms.assetid: e94de19c-de12-40fb-a72c-060f7ad12f75
ms.date: 12/05/2018
ms.keywords: GetTokenInformation, GetTokenInformation function [Security], _win32_gettokeninformation, security.gettokeninformation, securitybaseapi/GetTokenInformation
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetTokenInformation
 - securitybaseapi/GetTokenInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - GetTokenInformation
---

# GetTokenInformation function


## -description

The <b>GetTokenInformation</b> function retrieves a specified type of information about an <a href="/windows/desktop/SecGloss/a-gly">access token</a>. The calling process must have appropriate access rights to obtain the information.

To determine if a user is a member of a specific group, use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership">CheckTokenMembership</a> function. To determine group membership for app container tokens, use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembershipex">CheckTokenMembershipEx</a> function.

## -parameters

### -param TokenHandle [in]

A handle to an access token from which information is retrieved. If <i>TokenInformationClass</i> specifies TokenSource, the handle must have TOKEN_QUERY_SOURCE access. For all other <i>TokenInformationClass</i> values, the handle must have TOKEN_QUERY access.

### -param TokenInformationClass [in]

Specifies a value from the 
<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a> enumerated type to identify the type of information the function retrieves. Any callers who check the <b>TokenIsAppContainer</b> and have it return 0 should also verify that the caller token is not an identify level impersonation token. If the current token is not an app container but is an identity level token, you should return <b>AccessDenied</b>.

### -param TokenInformation [out, optional]

A pointer to a buffer the function fills with the requested information. The structure put into this buffer depends upon the type of information specified by the <i>TokenInformationClass</i> parameter.

### -param TokenInformationLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>TokenInformation</i> parameter. If <i>TokenInformation</i> is <b>NULL</b>, this parameter must be zero.

### -param ReturnLength [out]

A pointer to a variable that receives the number of bytes needed for the buffer pointed to by the <i>TokenInformation</i> parameter. If this value is larger than the value specified in the <i>TokenInformationLength</i> parameter, the function fails and stores no data in the buffer.

If the value of the <i>TokenInformationClass</i> parameter is TokenDefaultDacl and the token has no default DACL, the function sets the variable pointed to by <i>ReturnLength</i> to <code>sizeof(</code><a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a><code>)</code> and sets the <b>DefaultDacl</b> member of the <b>TOKEN_DEFAULT_DACL</b> structure to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership">CheckTokenMembership</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups_and_privileges">TOKEN_GROUPS_AND_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>