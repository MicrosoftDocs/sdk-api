---
UID: NF:securitybaseapi.SetTokenInformation
title: SetTokenInformation function (securitybaseapi.h)
description: Sets various types of information for a specified access token.
helpviewer_keywords: ["SetTokenInformation","SetTokenInformation function [Security]","_win32_settokeninformation","security.settokeninformation","securitybaseapi/SetTokenInformation"]
old-location: security\settokeninformation.htm
tech.root: security
ms.assetid: cdb8af74-540d-4059-ac64-6243f6aabaa6
ms.date: 12/05/2018
ms.keywords: SetTokenInformation, SetTokenInformation function [Security], _win32_settokeninformation, security.settokeninformation, securitybaseapi/SetTokenInformation
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
 - SetTokenInformation
 - securitybaseapi/SetTokenInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - SetTokenInformation
---

# SetTokenInformation function


## -description

The <b>SetTokenInformation</b> function sets various types of information for a specified <a href="/windows/desktop/SecGloss/a-gly">access token</a>. The information that this function sets replaces existing information. The calling process must have appropriate access rights to set the information.

## -parameters

### -param TokenHandle [in]

A handle to the access token for which information is to be set.

### -param TokenInformationClass [in]

A value from the 
<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a> enumerated type that identifies the type of information the function sets. The valid values from <b>TOKEN_INFORMATION_CLASS</b> are described in the <i>TokenInformation</i> parameter.

### -param TokenInformation [in]

A pointer to a buffer that contains the information set in the access token. The structure of this buffer depends on the type of information specified by the <i>TokenInformationClass</i> parameter.

### -param TokenInformationLength [in]

Specifies the length, in bytes, of the buffer pointed to by <i>TokenInformation</i>.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To set privilege information, an application can call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function. To set a token's groups, an application can call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a> function.

Token-type information can be set only when an access token is created.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>