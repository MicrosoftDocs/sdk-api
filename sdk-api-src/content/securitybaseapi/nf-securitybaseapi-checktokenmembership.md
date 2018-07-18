---
UID: NF:securitybaseapi.CheckTokenMembership
title: CheckTokenMembership function
author: windows-sdk-content
description: Determines whether a specified security identifier (SID) is enabled in an access token.
old-location: security\checktokenmembership.htm
old-project: secauthz
ms.assetid: c254a167-c4e7-4b84-9be3-6862761309f8
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: CheckTokenMembership, CheckTokenMembership function [Security], _win32_checktokenmembership, security.checktokenmembership, securitybaseapi/CheckTokenMembership
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
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
 - CheckTokenMembership
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# CheckTokenMembership function


## -description


The <b>CheckTokenMembership</b> function determines whether a specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) is enabled in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>. If you want to determine group membership for app container tokens, you need to use the <a href="https://msdn.microsoft.com/0420FC77-8035-42A5-8907-83D0CE53FB64">CheckTokenMembershipEx</a> function.


## -parameters




### -param TokenHandle [in, optional]

A handle to an access token. The handle must have TOKEN_QUERY access to the token. The token must be an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>. 




If <i>TokenHandle</i> is <b>NULL</b>, <b>CheckTokenMembership</b> uses the impersonation token of the calling thread. If the thread is not impersonating, the function duplicates the thread's <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> to create an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>.


### -param SidToCheck [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure. The <b>CheckTokenMembership</b> function checks for the presence of this SID in the user and group SIDs of the access token.


### -param IsMember [out]

A pointer to a variable that receives the results of the check. If the SID is present and has the SE_GROUP_ENABLED attribute, <i>IsMember</i> returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>CheckTokenMembership</b> function simplifies the process of determining whether a SID is both present and enabled in an access token.

Even if a SID is present in the token, the system may not use the SID in an access check. The SID may be disabled or have the <b>SE_GROUP_USE_FOR_DENY_ONLY</b> attribute. The system uses only enabled SIDs to grant access when performing an access check. For more information, see 
<a href="https://msdn.microsoft.com/c902f876-f05e-4b0c-ab65-a0c6cebca933">SID Attributes in an Access Token</a>.

If <i>TokenHandle</i> is a restricted token, or if <i>TokenHandle</i> is <b>NULL</b> and the current effective token of the calling thread is a restricted token, <b>CheckTokenMembership</b> also checks whether the SID is present in the list of restricting SIDs.


#### Examples

The following example shows checking a token for membership in the Administrators local group.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL IsUserAdmin(VOID)
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
    &amp;NtAuthority,
    2,
    SECURITY_BUILTIN_DOMAIN_RID,
    DOMAIN_ALIAS_RID_ADMINS,
    0, 0, 0, 0, 0, 0,
    &amp;AdministratorsGroup); 
if(b) 
{
    if (!CheckTokenMembership( NULL, AdministratorsGroup, &amp;b)) 
    {
         b = FALSE;
    } 
    FreeSid(AdministratorsGroup); 
}

return(b);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/0420FC77-8035-42A5-8907-83D0CE53FB64">CheckTokenMembershipEx</a>



<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>
 

 

