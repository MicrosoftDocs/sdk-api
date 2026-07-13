---
UID: NF:securitybaseapi.CheckTokenMembership
title: CheckTokenMembership function (securitybaseapi.h)
description: Determines whether a specified security identifier (SID) is enabled in an access token.
old-location: security\checktokenmembership.htm
tech.root: security
ms.assetid: c254a167-c4e7-4b84-9be3-6862761309f8
ms.date: 12/05/2018
ms.keywords: CheckTokenMembership, CheckTokenMembership function [Security], _win32_checktokenmembership, security.checktokenmembership, securitybaseapi/CheckTokenMembership
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
 - CheckTokenMembership
 - securitybaseapi/CheckTokenMembership
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
 - CheckTokenMembership
---

# CheckTokenMembership function


## -description

The <b>CheckTokenMembership</b> function determines whether a specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) is enabled in an <a href="/windows/desktop/SecGloss/a-gly">access token</a>. If you want to determine group membership for app container tokens, you need to use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembershipex">CheckTokenMembershipEx</a> function.

## -parameters

### -param TokenHandle [in, optional]

A handle to an access token. The handle must have TOKEN_QUERY access to the token. The token must be an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>. 




If <i>TokenHandle</i> is <b>NULL</b>, <b>CheckTokenMembership</b> uses the impersonation token of the calling thread. If the thread is not impersonating, the function duplicates the thread's <a href="/windows/desktop/SecGloss/p-gly">primary token</a> to create an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>.

### -param SidToCheck [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure. The <b>CheckTokenMembership</b> function checks for the presence of this SID in the user and group SIDs of the access token.

### -param IsMember [out]

A pointer to a variable that receives the results of the check. If the SID is present and has the SE_GROUP_ENABLED attribute, <i>IsMember</i> returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>CheckTokenMembership</b> function simplifies the process of determining whether a SID is both present and enabled in an access token.

Even if a SID is present in the token, the system may not use the SID in an access check. The SID may be disabled or have the <b>SE_GROUP_USE_FOR_DENY_ONLY</b> attribute. The system uses only enabled SIDs to grant access when performing an access check. For more information, see 
<a href="/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token">SID Attributes in an Access Token</a>.

If <i>TokenHandle</i> is a restricted token, or if <i>TokenHandle</i> is <b>NULL</b> and the current effective token of the calling thread is a restricted token, <b>CheckTokenMembership</b> also checks whether the SID is present in the list of restricting SIDs.


#### Examples

The following example shows checking a token for membership in the Administrators local group.


```cpp
BOOL IsUserAdmin(VOID)
/*++ 
Routine Description: This routine returns TRUE if the caller's
process is a member of the Administrators local group. Caller is NOT
expected to be impersonating anyone and is expected to be able to
open its own process and process token. 
Arguments: None. 
Return Value: 
   TRUE - Caller has Administrators local group. 
   FALSE - Caller does not have Administrators local group. --
*/ 
{
    BOOL b;
    SID_IDENTIFIER_AUTHORITY NtAuthority = SECURITY_NT_AUTHORITY;
    PSID AdministratorsGroup;
    b = AllocateAndInitializeSid(
        &NtAuthority,
        2,
        SECURITY_BUILTIN_DOMAIN_RID,
        DOMAIN_ALIAS_RID_ADMINS,
        0, 0, 0, 0, 0, 0,
        &AdministratorsGroup );

    if(b)
    {
        if (!CheckTokenMembership( NULL, AdministratorsGroup, &b))
        {
             b = FALSE;
        }
        FreeSid(AdministratorsGroup);
    }

    return(b);
}

```

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembershipex">CheckTokenMembershipEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>
