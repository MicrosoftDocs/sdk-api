---
UID: NF:securitybaseapi.AdjustTokenGroups
title: AdjustTokenGroups function (securitybaseapi.h)
description: Enables or disables groups already present in the specified access token. Access to TOKEN_ADJUST_GROUPS is required to enable or disable groups in an access token.
helpviewer_keywords: ["AdjustTokenGroups","AdjustTokenGroups function [Security]","_win32_adjusttokengroups","security.adjusttokengroups","securitybaseapi/AdjustTokenGroups"]
old-location: security\adjusttokengroups.htm
tech.root: security
ms.assetid: 839c4b58-4c61-4f72-8337-1e3dfa267ee5
ms.date: 12/05/2018
ms.keywords: AdjustTokenGroups, AdjustTokenGroups function [Security], _win32_adjusttokengroups, security.adjusttokengroups, securitybaseapi/AdjustTokenGroups
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
 - AdjustTokenGroups
 - securitybaseapi/AdjustTokenGroups
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
 - AdjustTokenGroups
---

# AdjustTokenGroups function


## -description

The <b>AdjustTokenGroups</b> function enables or disables groups already present in the specified <a href="/windows/desktop/SecGloss/a-gly">access token</a>. Access to TOKEN_ADJUST_GROUPS is required to enable or disable groups in an access token.

## -parameters

### -param TokenHandle [in]

A handle to the access token that contains the groups to be enabled or disabled. The handle must have TOKEN_ADJUST_GROUPS access to the token. If the <i>PreviousState</i> parameter is not <b>NULL</b>, the handle must also have TOKEN_QUERY access.

### -param ResetToDefault [in]

Boolean value that indicates whether the groups are to be set to their default enabled and disabled states. If this value is <b>TRUE</b>, the groups are set to their default states and the <i>NewState</i> parameter is ignored. If this value is <b>FALSE</b>, the groups are set according to the information pointed to by the <i>NewState</i> parameter.

### -param NewState [in, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the groups to be enabled or disabled. If the <i>ResetToDefault</i> parameter is <b>FALSE</b>, the function sets each of the groups to the value of that group's SE_GROUP_ENABLED attribute in the <b>TOKEN_GROUPS</b> structure. If <i>ResetToDefault</i> is <b>TRUE</b>, this parameter is ignored.

### -param BufferLength [in]

The size, in bytes, of the buffer pointed to by the <i>PreviousState</i> parameter. This parameter can be zero if the <i>PreviousState</i> parameter is <b>NULL</b>.

### -param PreviousState [out, optional]

A pointer to a buffer that receives a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure containing the previous state of any groups the function modifies. That is, if a group has been modified by this function, the group and its previous state are contained in the <b>TOKEN_GROUPS</b> structure referenced by <i>PreviousState</i>. If the <b>GroupCount</b> member of <b>TOKEN_GROUPS</b> is zero, then no groups have been changed by this function. This parameter can be <b>NULL</b>. 




If a buffer is specified but it does not contain enough space to receive the complete list of modified groups, no group states are changed and the function fails. In this case, the function sets the variable pointed to by the <i>ReturnLength</i> parameter to the number of bytes required to hold the complete list of modified groups.

### -param ReturnLength [out, optional]

A pointer to a variable that receives the actual number of bytes needed for the buffer pointed to by the <i>PreviousState</i> parameter. This parameter can be <b>NULL</b> and is ignored if <i>PreviousState</i> is <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The information retrieved in the <i>PreviousState</i> parameter is formatted as a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure. This means a pointer to the buffer can be passed as the <i>NewState</i> parameter in a subsequent call to the <b>AdjustTokenGroups</b> function, restoring the original state of the groups.

The <i>NewState</i> parameter can list groups to be changed that are not present in the access token. This does not affect the successful modification of the groups in the token.

The <b>AdjustTokenGroups</b> function cannot disable groups with the SE_GROUP_MANDATORY attribute in the <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure. Use 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a> instead.

You cannot enable a group that has the SE_GROUP_USE_FOR_DENY_ONLY attribute.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>