---
UID: NF:authz.AuthzInitializeContextFromSid
title: AuthzInitializeContextFromSid function (authz.h)
description: Creates a user-mode client context from a user security identifier (SID).
helpviewer_keywords: ["AUTHZ_COMPUTE_PRIVILEGES","AUTHZ_REQUIRE_S4U_LOGON","AUTHZ_SKIP_TOKEN_GROUPS","AuthzInitializeContextFromSid","AuthzInitializeContextFromSid function [Security]","_win32_authzinitializecontextfromsid","authz/AuthzInitializeContextFromSid","security.authzinitializecontextfromsid"]
old-location: security\authzinitializecontextfromsid.htm
tech.root: security
ms.assetid: 402a8641-5644-45c1-80e9-c60321c1ac38
ms.date: 12/05/2018
ms.keywords: AUTHZ_COMPUTE_PRIVILEGES, AUTHZ_REQUIRE_S4U_LOGON, AUTHZ_SKIP_TOKEN_GROUPS, AuthzInitializeContextFromSid, AuthzInitializeContextFromSid function [Security], _win32_authzinitializecontextfromsid, authz/AuthzInitializeContextFromSid, security.authzinitializecontextfromsid
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
 - AuthzInitializeContextFromSid
 - authz/AuthzInitializeContextFromSid
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
 - AuthzInitializeContextFromSid
---

# AuthzInitializeContextFromSid function


## -description

The <b>AuthzInitializeContextFromSid</b> function creates a user-mode client context from a user <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID). Domain SIDs retrieve token group attributes from the Active Directory. <div class="alert"><b>Note</b>  If possible, call the <a href="/windows/desktop/api/authz/nf-authz-authzinitializecontextfromtoken">AuthzInitializeContextFromToken</a>  function instead of <b>AuthzInitializeContextFromSid</b>. For more information, see  Remarks.</div>
<div> </div>

## -parameters

### -param Flags [in]

The following flags are defined. 

Starting with Windows 8 and Windows Server 2012,  when you call this function on a remote context handle, the upper 16 bits must be zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
Default value.

<b>AuthzInitializeContextFromSid</b> attempts to retrieve the user's token group information by performing an S4U logon.

If S4U logon is not supported by the user's domain or the calling computer, <b>AuthzInitializeContextFromSid</b> queries the user's account object for group information. When an account is queried directly, some groups that represent logon characteristics, such as Network, Interactive, Anonymous, Network Service, or Local Service, are omitted. Applications can explicitly add such group SIDs by implementing the <a href="/windows/desktop/SecAuthZ/authzcomputegroupscallback">AuthzComputeGroupsCallback</a> function or calling the <a href="/windows/desktop/api/authz/nf-authz-authzaddsidstocontext">AuthzAddSidsToContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SKIP_TOKEN_GROUPS"></a><a id="authz_skip_token_groups"></a><dl>
<dt><b>AUTHZ_SKIP_TOKEN_GROUPS</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Causes <b>AuthzInitializeContextFromSid</b> to skip all group evaluations. When this flag is used, the context returned contains only the SID specified by the <i>UserSid</i> parameter. The specified SID can be an arbitrary or application-specific SID. Other SIDs can be added to this context by implementing the <a href="/windows/desktop/SecAuthZ/authzcomputegroupscallback">AuthzComputeGroupsCallback</a> function or by calling the <a href="/windows/desktop/api/authz/nf-authz-authzaddsidstocontext">AuthzAddSidsToContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_REQUIRE_S4U_LOGON"></a><a id="authz_require_s4u_logon"></a><dl>
<dt><b>AUTHZ_REQUIRE_S4U_LOGON</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
Causes <b>AuthzInitializeContextFromSid</b> to fail if Windows Services For User is not available to retrieve token group information.

<b>Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_COMPUTE_PRIVILEGES"></a><a id="authz_compute_privileges"></a><dl>
<dt><b>AUTHZ_COMPUTE_PRIVILEGES</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
Causes <b>AuthzInitializeContextFromSid</b> to retrieve privileges for the new context. If this function performs an S4U logon, it retrieves privileges from the token. Otherwise, the function retrieves privileges from all SIDs in the context.

</td>
</tr>
</table>

### -param UserSid [in]

The SID of the user for whom a client context will be created. This must be a valid user or computer account unless the AUTHZ_SKIP_TOKEN_GROUPS flag is used.

### -param hAuthzResourceManager [in, optional]

A handle to the resource manager creating this client context. This handle is stored in the client context structure. 

Starting with Windows 8 and Windows Server 2012, the resource manager can be local or remote and is obtained by calling the <a href="/windows/desktop/api/authz/nf-authz-authzinitializeremoteresourcemanager">AuthzInitializeRemoteResourceManager</a> function.

### -param pExpirationTime [in]

Expiration date and time of the token. If no value is passed, the token never expires. Expiration time is not currently enforced.

### -param Identifier [in]

Specific identifier of the resource manager. This parameter is not currently used.

### -param DynamicGroupArgs [in, optional]

A pointer to parameters to be passed to the callback function that computes dynamic groups. This parameter can be <b>NULL</b> if no dynamic parameters are passed to the callback function. 

Starting with Windows 8 and Windows Server 2012, this parameter must be  <b>NULL</b> if the resource manager is remote. Otherwise, ERROR_NOT_SUPPORTED will be set.

### -param phAuthzClientContext [out]

A pointer to the handle to the client context that the <b>AuthzInitializeContextFromSid</b> function creates.  When you have finished using the handle, free it by calling the <a href="/windows/desktop/api/authz/nf-authz-authzfreecontext">AuthzFreeContext</a> function.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If possible, call the <a href="/windows/desktop/api/authz/nf-authz-authzinitializecontextfromtoken">AuthzInitializeContextFromToken</a>  function instead of <b>AuthzInitializeContextFromSid</b>. <b>AuthzInitializeContextFromSid</b> attempts to retrieve the information available in a logon token had the client actually logged on. An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon. The client context  created by <b>AuthzInitializeContextFromToken</b> uses a logon token, and the resulting client context is more complete and accurate than a client context created by <b>AuthzInitializeContextFromSid</b>.

This function resolves valid user SIDs only.

<b>Windows XP:  </b>This function resolves group memberships for valid user and group SIDs (unless the AUTHZ_SKIP_TOKEN_GROUPS flag is used). Support for resolving memberships of group SIDs may be altered or unavailable in subsequent versions.

This function calls the  <a href="/windows/desktop/SecAuthZ/authzcomputegroupscallback">AuthzComputeGroupsCallback</a> callback function to add SIDs to the newly created context.

<div class="alert"><b>Important</b>  Applications should not assume that the calling context has permission to use this function. The <b>AuthzInitializeContextFromSid</b> function reads the tokenGroupsGlobalAndUniversal attribute of the SID specified in the call to determine the current user's group memberships. If the user's object is in <a href="/windows/desktop/AD/active-directory-domain-services">Active Directory</a>, the calling context must have read access to the tokenGroupsGlobalAndUniversal attribute on the user object. When a new domain is created, the default access compatibility selection is <b>Permissions compatible with Windows 2000 and Windows Server 2003 operating systems</b>. When this option is set, the  <b>Pre-Windows 2000 Compatible Access</b> group includes only the <b>Authenticated Users</b>  built-in security identifiers. Therefore, applications may not have access to the tokenGroupsGlobalAndUniversal attribute; in this case, the <b>AuthzInitializeContextFromSid</b> function  fails with ACCESS_DENIED. Applications that use this function should correctly handle this error and provide supporting documentation. To simplify granting accounts permission to query a user's group information, add accounts that need the ability to look up group information to the Windows Authorization Access Group.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Allowing Anonymous Access</a>



<a href="/windows/desktop/api/authz/nf-authz-authzfreecontext">AuthzFreeContext</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>