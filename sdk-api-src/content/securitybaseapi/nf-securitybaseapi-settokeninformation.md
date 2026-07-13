---
UID: NF:securitybaseapi.SetTokenInformation
title: SetTokenInformation function (securitybaseapi.h)
description: Sets various types of information for a specified access token.
helpviewer_keywords: ["SetTokenInformation","SetTokenInformation function [Security]","_win32_settokeninformation","security.settokeninformation","securitybaseapi/SetTokenInformation"]
old-location: security\settokeninformation.htm
tech.root: security
ms.assetid: cdb8af74-540d-4059-ac64-6243f6aabaa6
ms.date: 02/19/2025
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
 - SetTokenInformation
---

# SetTokenInformation function

## -description

The **SetTokenInformation** function sets various types of information for a specified [access token](/windows/win32/SecGloss/a-gly). The information that this function sets replaces existing information. The calling process must have appropriate access rights to set the information.

## -parameters

### -param TokenHandle [in]

A handle to the access token for which information is to be set.

### -param TokenInformationClass [in]

A value from the [TOKEN_INFORMATION_CLASS](/windows/win32/api/winnt/ne-winnt-token_information_class) enumerated type that identifies the type of information the function sets from the *TokenInformation* parameter.

### -param TokenInformation [in]

A pointer to a buffer that contains the information set in the access token. The structure of this buffer depends on the type of information specified by the *TokenInformationClass* parameter.

### -param TokenInformationLength [in]

Specifies the length, in bytes, of the buffer pointed to by *TokenInformation*.

## -returns

If the function succeeds, the function returns a non-zero value.

If the function fails, it returns zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

To set privilege information, an application can call the [AdjustTokenPrivileges](nf-securitybaseapi-adjusttokenprivileges.md) function. To set a token's groups, an application can call the [AdjustTokenGroups](nf-securitybaseapi-adjusttokengroups.md) function.

Token-type information can be set only when an access token is created.

## -see-also

[Access Control Overview](/windows/win32/SecAuthZ/access-control)

[AdjustTokenGroups](nf-securitybaseapi-adjusttokengroups.md)

[AdjustTokenPrivileges](nf-securitybaseapi-adjusttokenprivileges.md)

[Basic Access Control Functions](/windows/win32/SecAuthZ/authorization-functions)

[GetTokenInformation](nf-securitybaseapi-gettokeninformation.md)

[OpenProcessToken](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)

[OpenThreadToken](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)

[TOKEN_DEFAULT_DACL](/windows/win32/api/winnt/ns-winnt-token_default_dacl)

[TOKEN_INFORMATION_CLASS](/windows/win32/api/winnt/ne-winnt-token_information_class)

[TOKEN_OWNER](/windows/win32/api/winnt/ns-winnt-token_owner)

[TOKEN_PRIMARY_GROUP](/windows/win32/api/winnt/ns-winnt-token_primary_group)
