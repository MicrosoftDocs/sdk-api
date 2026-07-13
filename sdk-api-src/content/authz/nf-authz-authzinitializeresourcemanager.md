---
UID: NF:authz.AuthzInitializeResourceManager
title: AuthzInitializeResourceManager function (authz.h)
description: Uses Authz to verify that clients have access to various resources.
helpviewer_keywords: ["AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION","AUTHZ_RM_FLAG_NO_AUDIT","AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES","AuthzInitializeResourceManager","AuthzInitializeResourceManager function [Security]","_win32_authzinitializeresourcemanager","authz/AuthzInitializeResourceManager","security.authzinitializeresourcemanager"]
old-location: security\authzinitializeresourcemanager.htm
tech.root: security
ms.assetid: e3f6b37d-2c33-4b17-97b4-762bf55561c5
ms.date: 12/05/2018
ms.keywords: AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION, AUTHZ_RM_FLAG_NO_AUDIT, AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES, AuthzInitializeResourceManager, AuthzInitializeResourceManager function [Security], _win32_authzinitializeresourcemanager, authz/AuthzInitializeResourceManager, security.authzinitializeresourcemanager
req.header: authz.h
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - AuthzInitializeResourceManager
 - authz/AuthzInitializeResourceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
 - Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
 - AuthzInitializeResourceManager
---

# AuthzInitializeResourceManager function


## -description

The <b>AuthzInitializeResourceManager</b> function uses Authz to verify that clients have access to various resources.

## -parameters

### -param Flags [in]

A <b>DWORD</b> value that defines how the resource manager is initialized. This parameter can contain the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Default call to the function. The resource manager is initialized as the principal identified in the process token, and auditing is in effect. Note that unless the <b>AUTHZ_RM_FLAG_NO_AUDIT</b> flag is set, <b>SeAuditPrivilege</b> must be enabled for the function to succeed.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_RM_FLAG_NO_AUDIT"></a><a id="authz_rm_flag_no_audit"></a><dl>
<dt><b>AUTHZ_RM_FLAG_NO_AUDIT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Auditing is not in effect. If this flag is set, the caller does not need to have <b>SeAuditPrivilege</b> enabled to call this function.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION"></a><a id="authz_rm_flag_initialize_under_impersonation"></a><dl>
<dt><b>AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The resource manager is initialized as the identity of the thread token.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES"></a><a id="authz_rm_flag_no_central_access_policies"></a><dl>
<dt><b>AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The resource manager ignores CAP IDs and does not evaluate centralized access policies.

</td>
</tr>
</table>
 

AUTHZ_RM_FLAG_NO_AUDIT and AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION can be bitwise-combined.

### -param pfnDynamicAccessCheck [in, optional]

A pointer to the <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> callback function that the resource manager calls each time it encounters a callback
						<a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) during <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) evaluation in 
<a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> or 
<a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a>.  This parameter can be <b>NULL</b> if no access check callback function is used.

### -param pfnComputeDynamicGroups [in, optional]

A pointer to the <a href="/windows/desktop/SecAuthZ/authzcomputegroupscallback">AuthzComputeGroupsCallback</a> callback function called by the resource manager during initialization of an <i>AuthzClientContext</i> handle. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.

### -param pfnFreeDynamicGroups [in, optional]

A pointer to the <a href="/windows/desktop/SecAuthZ/authzfreegroupscallback">AuthzFreeGroupsCallback</a> callback function called by the resource manager to free <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) attribute arrays allocated by the compute dynamic groups callback. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.

### -param szResourceManagerName [in]

A string that identifies the resource manager. This parameter can be <b>NULL</b> if the resource manager does not need a name.

### -param phAuthzResourceManager [out]

A pointer to the returned resource manager handle. When you have finished using the handle, free it by calling the <a href="/windows/desktop/api/authz/nf-authz-authzfreeresourcemanager">AuthzFreeResourceManager</a> function.

## -returns

If the function succeeds, the function returns a nonzero value. 

If the function fails, it returns a zero value. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a>



<a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a>



<a href="/windows/desktop/api/authz/nf-authz-authzfreeresourcemanager">AuthzFreeResourceManager</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>
