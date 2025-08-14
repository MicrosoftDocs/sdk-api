---
UID: NF:securitybaseapi.PrivilegeCheck
title: PrivilegeCheck function (securitybaseapi.h)
description: Determines whether a specified set of privileges are enabled in an access token.
helpviewer_keywords: ["PrivilegeCheck","PrivilegeCheck function [Security]","_win32_privilegecheck","security.privilegecheck","securitybaseapi/PrivilegeCheck"]
old-location: security\privilegecheck.htm
tech.root: security
ms.assetid: a73d934a-1abf-4e60-bf0a-6c4629f28f7a
ms.date: 12/05/2018
ms.keywords: PrivilegeCheck, PrivilegeCheck function [Security], _win32_privilegecheck, security.privilegecheck, securitybaseapi/PrivilegeCheck
req.header: securitybaseapi.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PrivilegeCheck
 - securitybaseapi/PrivilegeCheck
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
 - PrivilegeCheck
---

# PrivilegeCheck function


## -description

The <b>PrivilegeCheck</b> function determines whether a specified set of 
<a href="/windows/desktop/SecAuthZ/privileges">privileges</a> are enabled in an <a href="/windows/desktop/SecGloss/a-gly">access token</a>. The <b>PrivilegeCheck</b> function is typically called by a server application to check the privileges of a client's access token.

## -parameters

### -param ClientToken [in]

A handle to an access token representing a client <a href="/windows/desktop/SecGloss/p-gly">process</a>. This handle must have been obtained by opening the token of a thread impersonating the client. The token must be open for TOKEN_QUERY access.

### -param RequiredPrivileges [in, out]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure. The <b>Privilege</b> member of this structure is an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-luid_and_attributes">LUID_AND_ATTRIBUTES</a> structures. Before calling <b>PrivilegeCheck</b>, use the <b>Privilege</b> array to indicate the set of privileges to check. Set the <b>Control</b> member to PRIVILEGE_SET_ALL_NECESSARY if all of the privileges must be enabled; or set it to zero if it is sufficient that any one of the privileges be enabled. 




When <b>PrivilegeCheck</b> returns, the <b>Attributes</b> member of each <a href="/windows/desktop/api/winnt/ns-winnt-luid_and_attributes">LUID_AND_ATTRIBUTES</a> structure is set to SE_PRIVILEGE_USED_FOR_ACCESS if the corresponding privilege is enabled.

### -param pfResult [out]

A pointer to a value the function sets to indicate whether any or all of the specified privileges are enabled in the access token. If the <b>Control</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure specifies PRIVILEGE_SET_ALL_NECESSARY, this value is <b>TRUE</b> only if all the privileges are enabled; otherwise, this value is <b>TRUE</b> if any of the privileges are enabled.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An access token contains a list of the privileges held by the account associated with the token. These privileges can be enabled or disabled; most are disabled by default. The <b>PrivilegeCheck</b> function checks only for enabled privileges. To get a list of all the enabled and disabled privileges held by an access token, call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function. To enable or disable a set of privileges in an access token, call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-luid_and_attributes">LUID_AND_ATTRIBUTES</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegevaluea">LookupPrivilegeValue</a>



<a href="/windows/desktop/api/winbase/nf-winbase-objectprivilegeauditalarma">ObjectPrivilegeAuditAlarm</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/winbase/nf-winbase-privilegedserviceauditalarma">PrivilegedServiceAuditAlarm</a>