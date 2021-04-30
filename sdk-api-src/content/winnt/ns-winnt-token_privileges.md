---
UID: NS:winnt._TOKEN_PRIVILEGES
title: TOKEN_PRIVILEGES (winnt.h)
description: Contains information about a set of privileges for an access token.
helpviewer_keywords: ["*PTOKEN_PRIVILEGES","PTOKEN_PRIVILEGES","PTOKEN_PRIVILEGES structure pointer [Security]","SE_PRIVILEGE_ENABLED","SE_PRIVILEGE_ENABLED_BY_DEFAULT","SE_PRIVILEGE_REMOVED","SE_PRIVILEGE_USED_FOR_ACCESS","TOKEN_PRIVILEGES","TOKEN_PRIVILEGES structure [Security]","_TOKEN_PRIVILEGES","_win32_token_privileges_str","security.token_privileges","winnt/PTOKEN_PRIVILEGES","winnt/TOKEN_PRIVILEGES"]
old-location: security\token_privileges.htm
tech.root: security
ms.assetid: c9016511-740f-44f3-92ed-17cc518c6612
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_PRIVILEGES, PTOKEN_PRIVILEGES, PTOKEN_PRIVILEGES structure pointer [Security], SE_PRIVILEGE_ENABLED, SE_PRIVILEGE_ENABLED_BY_DEFAULT, SE_PRIVILEGE_REMOVED, SE_PRIVILEGE_USED_FOR_ACCESS, TOKEN_PRIVILEGES, TOKEN_PRIVILEGES structure [Security], _TOKEN_PRIVILEGES, _win32_token_privileges_str, security.token_privileges, winnt/PTOKEN_PRIVILEGES, winnt/TOKEN_PRIVILEGES'
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TOKEN_PRIVILEGES, *PTOKEN_PRIVILEGES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_PRIVILEGES
 - winnt/_TOKEN_PRIVILEGES
 - PTOKEN_PRIVILEGES
 - winnt/PTOKEN_PRIVILEGES
 - TOKEN_PRIVILEGES
 - winnt/TOKEN_PRIVILEGES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_PRIVILEGES
---

# TOKEN_PRIVILEGES structure


## -description

The <b>TOKEN_PRIVILEGES</b> structure contains information about a set of privileges for an <a href="/windows/desktop/SecGloss/a-gly">access token</a>.

## -struct-fields

### -field PrivilegeCount

This must be set to the number of entries in the <b>Privileges</b> array.

### -field Privileges

Specifies an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-luid_and_attributes">LUID_AND_ATTRIBUTES</a> structures. Each structure contains the 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> and attributes of a privilege. To get the name of the privilege associated with a  <b>LUID</b>, call the <a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegenamea">LookupPrivilegeName</a> function, passing the address of the <b>LUID</b> as the value of the <i>lpLuid</i> parameter.

<div class="alert"><b>Important</b>  The constant<b> ANYSIZE_ARRAY</b> is defined as 1 in the public header Winnt.h. To create this array with more than one element, you must allocate sufficient memory for the structure to take into account additional elements.</div>
<div> </div>
The attributes of a privilege can be a combination of the following values. 




					

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
The privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_ENABLED_BY_DEFAULT"></a><a id="se_privilege_enabled_by_default"></a><dl>
<dt><b>SE_PRIVILEGE_ENABLED_BY_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The privilege is enabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_REMOVED"></a><a id="se_privilege_removed"></a><dl>
<dt><b>SE_PRIVILEGE_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
Used to remove a privilege. For details, see <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_USED_FOR_ACCESS"></a><a id="se_privilege_used_for_access"></a><dl>
<dt><b>SE_PRIVILEGE_USED_FOR_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
The privilege was used to gain access to an object or service. This flag is used to identify the relevant privileges in a set passed by a client application that may contain unnecessary privileges.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-luid_and_attributes">LUID_AND_ATTRIBUTES</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegenamea">LookupPrivilegeName</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-privilegedserviceauditalarma">PrivilegedServiceAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>