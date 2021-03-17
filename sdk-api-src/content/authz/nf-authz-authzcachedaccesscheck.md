---
UID: NF:authz.AuthzCachedAccessCheck
title: AuthzCachedAccessCheck function (authz.h)
description: Performs a fast access check based on a cached handle containing the static granted bits from a previous AuthzAccessCheck call.
helpviewer_keywords: ["AuthzCachedAccessCheck","AuthzCachedAccessCheck function [Security]","_win32_authzcachedaccesscheck","authz/AuthzCachedAccessCheck","security.authzcachedaccesscheck"]
old-location: security\authzcachedaccesscheck.htm
tech.root: security
ms.assetid: 8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4
ms.date: 12/05/2018
ms.keywords: AuthzCachedAccessCheck, AuthzCachedAccessCheck function [Security], _win32_authzcachedaccesscheck, authz/AuthzCachedAccessCheck, security.authzcachedaccesscheck
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
 - AuthzCachedAccessCheck
 - authz/AuthzCachedAccessCheck
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
 - AuthzCachedAccessCheck
---

# AuthzCachedAccessCheck function


## -description

The <b>AuthzCachedAccessCheck</b> function performs a fast access check based on a cached handle containing the static granted bits from a previous 
<a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> call.

## -parameters

### -param Flags [in]

Reserved for future use.

### -param hAccessCheckResults [in]

A handle to the cached access check results.

### -param pRequest [in]

Access request handle specifying the desired <a href="/windows/desktop/SecGloss/a-gly">access mask</a>, principal self <a href="/windows/desktop/SecGloss/s-gly">SID</a>, and the object type list structure (if any).

### -param hAuditEvent [in]

A structure that contains object-specific audit information. When the value of this parameter is not null, an audit is automatically requested. Static audit information is read from the resource manager structure.

### -param pReply [out]

A pointer to an 
<a href="/windows/desktop/api/authz/ns-authz-authz_access_reply">AUTHZ_ACCESS_REPLY</a> handle that returns the results of access check as an array of GrantedAccessMask/ErrorValue pairs. The number of pairs returned is supplied by the caller in the <b>ResultListLength</b> member of the <b>AUTHZ_ACCESS_REPLY</b> structure.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Expected values of the Error members of array elements returned are shown in the following table.

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
All the access bits, not including MAXIMUM_ALLOWED, are granted and the <b>GrantedAccessMask</b> member of the <i>pReply</i> parameter  is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PRIVILEGE_NOT_HELD</b></dt>
</dl>
</td>
<td width="60%">
The <b>DesiredAccess</b> member of the <i>pRequest</i> parameter includes ACCESS_SYSTEM_SECURITY, and the client does not have the SeSecurityPrivilege privilege.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
One or more of the following is true: 




<ul>
<li>The requested bits are not granted.</li>
<li>The MaximumAllowed bit is on, and the granted access is zero.</li>
<li>The <b>DesiredAccess</b> member of the <i>pRequest</i> parameter is zero.</li>
</ul>
</td>
</tr>
</table>

## -remarks

The client context pointer is stored in the <i>AuthzHandle</i> parameter. The structure of the client context must be exactly the same as it was at the time <i>AuthzHandle</i> was created. This restriction is for the following fields:

<ul>
<li>SIDs</li>
<li>RestrictedSids</li>
<li>Privileges</li>
</ul>
Pointers to the primary <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> and the optional security descriptor array are stored in <i>AuthzHandle</i> at the time of handle creation. These pointers must still be valid. 

The <b>AuthzCachedAccessCheck</b> function maintains a cache as a result of evaluating Central Access Policies (CAP) on objects unless CAPs are ignored, for example when the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is used. The client may call the <a href="/windows/desktop/api/authz/nf-authz-authzfreecentralaccesspolicycache">AuthzFreeCentralAccessPolicyCache</a> function to free up this cache. Note that this requires a subsequent call to <b>AuthzCachedAccessCheck</b> to rebuild the cache if necessary. 

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> and <a href="/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a> overviews.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_access_reply">AUTHZ_ACCESS_REPLY</a>



<a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a>



<a href="/windows/desktop/api/authz/nf-authz-authzfreecentralaccesspolicycache">AuthzFreeCentralAccessPolicyCache</a>



<a href="/windows/desktop/api/authz/nf-authz-authzinitializeresourcemanager">AuthzInitializeResourceManager</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>