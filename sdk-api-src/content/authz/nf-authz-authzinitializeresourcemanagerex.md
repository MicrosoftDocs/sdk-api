---
UID: NF:authz.AuthzInitializeResourceManagerEx
title: AuthzInitializeResourceManagerEx function (authz.h)
description: Allocates and initializes a resource manager structure.
helpviewer_keywords: ["AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION","AUTHZ_RM_FLAG_NO_AUDIT","AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES","AuthzInitializeResourceManagerEx","AuthzInitializeResourceManagerEx function [Security]","authz/AuthzInitializeResourceManagerEx","security.authzinitializeresourcemanagerex"]
old-location: security\authzinitializeresourcemanagerex.htm
tech.root: security
ms.assetid: CDB78606-1B53-4516-90E6-1FF096B3D7D9
ms.date: 12/05/2018
ms.keywords: AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION, AUTHZ_RM_FLAG_NO_AUDIT, AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES, AuthzInitializeResourceManagerEx, AuthzInitializeResourceManagerEx function [Security], authz/AuthzInitializeResourceManagerEx, security.authzinitializeresourcemanagerex
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuthzInitializeResourceManagerEx
 - authz/AuthzInitializeResourceManagerEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzInitializeResourceManagerEx
---

# AuthzInitializeResourceManagerEx function


## -description

The <b>AuthzInitializeResourceManagerEx</b> function initializes an Authz resource manager and returns a handle to it. Use this function rather than <a href="/windows/desktop/api/authz/nf-authz-authzinitializeresourcemanager">AuthzInitializeResourceManager</a> when you want the resource manager to manage Central Access Policies (CAPs).

## -parameters

### -param Flags [in, optional]

A <b>DWORD</b> value that defines how the resource manager is initialized. This parameter can be one or more of the following values.

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
Default call to the function. The resource manager is initialized as the principal identified in the process token, and auditing is in effect. Unless the <b>AUTHZ_RM_FLAG_NO_AUDIT</b> flag is set, <b>SeAuditPrivilege</b> must be enabled for the function to succeed.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_RM_FLAG_NO_AUDIT"></a><a id="authz_rm_flag_no_audit"></a><dl>
<dt><b>AUTHZ_RM_FLAG_NO_AUDIT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Auditing is not in effect. If this flag is set, the caller does not need to have <b>SeAuditPrivilege</b> enabled to call this function. Use this flag if the resource manager will never generate an audit for best performance.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION"></a><a id="authz_rm_flag_initialize_under_impersonation"></a><dl>
<dt><b>AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The resource manager is initialized as the identity of the thread token. If the current thread is impersonating, then use the impersonation token as the identity of the resource manager.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES"></a><a id="authz_rm_flag_no_central_access_policies"></a><dl>
<dt><b>AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The central access policy IDs are ignored. Do not evaluate central access policies. 

</td>
</tr>
</table>

### -param pAuthzInitInfo [in, optional]

A pointer to a <a href="/windows/desktop/api/authz/ns-authz-authz_init_info">AUTHZ_INIT_INFO</a> structure that contains the authorization resource manager initialization information.

### -param phAuthzResourceManager [out]

A pointer to the returned resource manager handle. When you have finished using the handle, free it by using the <a href="/windows/desktop/api/authz/nf-authz-authzfreeresourcemanager">AuthzFreeResourceManager</a> function.

## -returns

If the function succeeds, the function returns a value of <b>TRUE</b>. 

If the function fails, it returns a value of <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is specified, then <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> and <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a> ignore CAPID (Central Access Policie ID) <a href="/windows/desktop/SecGloss/a-gly">access control entries</a><a href="/windows/desktop/api/winnt/ns-winnt-system_scoped_policy_id_ace">SYSTEM_SCOPED_POLICY_ID_ACE</a> and will not evaluate CAPs.

If the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is not specified and pfnGetCentralAccessPolicy is <b>NULL</b>, then <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> and <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a> will get CAPs from LSA. For more information, see <a href="/windows/desktop/api/ntlsa/nf-ntlsa-lsagetappliedcapids">LsaGetAppliedCAPIDs</a>.

If the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is not specified and a central access policy callback is provided by the resource manager, then <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> and <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a> will get CAPs from the resource manager by invoking the callback.

The LSA and the central access policy callback can indicate that CAPs are not supported, in which case <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> and <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a> ignore CAPID ACEs and will not evaluate CAPs.

The LSA and the central access policy callback may fail to return a CAP that corresponds to a particular CAPID, in which case <b>AuthzAccessCheck</b> and <b>AuthzCachedAccessCheck</b> use the same default CAP as the kernel AccessCheck.

## -see-also

<a href="/windows/desktop/api/ntlsa/nf-ntlsa-lsagetappliedcapids">LsaGetAppliedCAPIDs</a>