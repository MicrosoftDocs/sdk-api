---
UID: NF:securitybaseapi.AdjustTokenPrivileges
title: AdjustTokenPrivileges function (securitybaseapi.h)
description: Enables or disables privileges in the specified access token. Enabling or disabling privileges in an access token requires TOKEN_ADJUST_PRIVILEGES access.
helpviewer_keywords: ["AdjustTokenPrivileges","AdjustTokenPrivileges function [Security]","None","SE_PRIVILEGE_ENABLED","SE_PRIVILEGE_REMOVED","_win32_adjusttokenprivileges","security.adjusttokenprivileges","securitybaseapi/AdjustTokenPrivileges"]
old-location: security\adjusttokenprivileges.htm
tech.root: security
ms.assetid: 8e3f70cd-814e-4aab-8f48-0ca482beef2e
ms.date: 12/05/2018
ms.keywords: AdjustTokenPrivileges, AdjustTokenPrivileges function [Security], None, SE_PRIVILEGE_ENABLED, SE_PRIVILEGE_REMOVED, _win32_adjusttokenprivileges, security.adjusttokenprivileges, securitybaseapi/AdjustTokenPrivileges
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
 - AdjustTokenPrivileges
 - securitybaseapi/AdjustTokenPrivileges
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
 - AdjustTokenPrivileges
---

# AdjustTokenPrivileges function


## -description

The <b>AdjustTokenPrivileges</b> function enables or disables privileges in the specified <a href="/windows/desktop/SecGloss/a-gly">access token</a>. Enabling or disabling privileges in an access token requires TOKEN_ADJUST_PRIVILEGES access.

## -parameters

### -param TokenHandle [in]

A handle to the access token that contains the privileges to be modified. The handle must have TOKEN_ADJUST_PRIVILEGES access to the token. If the <i>PreviousState</i> parameter is not <b>NULL</b>, the handle must also have TOKEN_QUERY access.

### -param DisableAllPrivileges [in]

Specifies whether the function disables all of the token's privileges. If this value is <b>TRUE</b>, the function disables all privileges and ignores the <i>NewState</i> parameter. If it is <b>FALSE</b>, the function modifies privileges based on the information pointed to by the <i>NewState</i> parameter.

### -param NewState [in, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that specifies an array of privileges and their attributes. If the <i>DisableAllPrivileges</i> parameter is <b>FALSE</b>, the  <b>AdjustTokenPrivileges</b>  function enables, disables, or removes these privileges for the token. The following table describes the action taken by the <b>AdjustTokenPrivileges</b> function, based on the privilege attribute.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_ENABLED"></a><a id="se_privilege_enabled"></a><dl>
<dt><b>SE_PRIVILEGE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The function enables the privilege.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_REMOVED"></a><a id="se_privilege_removed"></a><dl>
<dt><b>SE_PRIVILEGE_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
The privilege is removed from the list of privileges in the token. The other privileges in the list are reordered to remain contiguous.
           

SE_PRIVILEGE_REMOVED supersedes SE_PRIVILEGE_ENABLED.

Because the privilege has been removed from the token, attempts to reenable the privilege result in the warning ERROR_NOT_ALL_ASSIGNED as if the privilege had never existed.

Attempting to remove a privilege that does not exist in the token results in ERROR_NOT_ALL_ASSIGNED being returned.

Privilege checks for removed privileges result in STATUS_PRIVILEGE_NOT_HELD.  Failed privilege check auditing occurs as normal.

The removal of the privilege is irreversible, so the name of the removed privilege is not included in the <i>PreviousState</i> parameter after a call to <b>AdjustTokenPrivileges</b>.

<b>Windows XP with SP1:  </b>The function cannot remove privileges. This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="None"></a><a id="none"></a><a id="NONE"></a><dl>
<dt><b>None</b></dt>
</dl>
</td>
<td width="60%">
The function disables the privilege.

</td>
</tr>
</table>
 

If <i>DisableAllPrivileges</i> is <b>TRUE</b>, the function ignores this parameter.

### -param BufferLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>PreviousState</i> parameter. This parameter can be zero if the <i>PreviousState</i> parameter is <b>NULL</b>.

### -param PreviousState [out, optional]

A pointer to a buffer that the function fills with a <a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that contains the previous state of any privileges that the function modifies.  That is, if a privilege has been modified by this function, the privilege and its previous state are contained in the <b>TOKEN_PRIVILEGES</b> structure referenced by <i>PreviousState</i>. If the <b>PrivilegeCount</b> member of <b>TOKEN_PRIVILEGES</b> is zero, then no privileges have been changed by this function. This parameter can be <b>NULL</b>. 




If you specify a buffer that is too small to receive the complete list of modified privileges, the function fails and does not adjust any privileges. In this case, the function sets the variable pointed to by the <i>ReturnLength</i> parameter to the number of bytes required to hold the complete list of modified privileges.

### -param ReturnLength [out, optional]

A pointer to a variable that receives the required size, in bytes, of the buffer pointed to by the <i>PreviousState</i> parameter. This parameter can be <b>NULL</b> if <i>PreviousState</i> is <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero. To determine whether the function adjusted all of the specified privileges, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns one of the following values when the function succeeds:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function adjusted all specified privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ALL_ASSIGNED</b></dt>
</dl>
</td>
<td width="60%">
The token does not have one or more of the privileges specified in the <i>NewState</i> parameter. The function may succeed with this error value even if no privileges were adjusted. The <i>PreviousState</i> parameter indicates the privileges that were adjusted.

</td>
</tr>
</table>
 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>AdjustTokenPrivileges</b> function cannot add new privileges to the access token. It can only enable or disable the token's existing privileges. To determine the token's privileges, call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function.

The <i>NewState</i> parameter can specify privileges that the token does not have, without causing the function to fail. In this case, the function adjusts the privileges that the token does have and ignores the other privileges so that the function succeeds. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to determine whether the function adjusted all of the specified privileges. The <i>PreviousState</i> parameter indicates the privileges that were adjusted.

The <i>PreviousState</i> parameter retrieves a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that contains the original state of the adjusted privileges. To restore the original state, pass the <i>PreviousState</i> pointer as the <i>NewState</i> parameter in a subsequent call to the <b>AdjustTokenPrivileges</b> function.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--">Enabling and Disabling Privileges</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>