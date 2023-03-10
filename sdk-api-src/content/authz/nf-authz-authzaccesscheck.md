---
UID: NF:authz.AuthzAccessCheck
title: AuthzAccessCheck function (authz.h)
description: Determines which access bits can be granted to a client for a given set of security descriptors.
helpviewer_keywords: ["AUTHZ_ACCESS_CHECK_NO_DEEP_COPY_SD","AuthzAccessCheck","AuthzAccessCheck function [Security]","_win32_authzaccesscheck","authz/AuthzAccessCheck","security.authzaccesscheck"]
old-location: security\authzaccesscheck.htm
tech.root: security
ms.assetid: 633c2a73-169c-4e0c-abb6-96c360bd63cf
ms.date: 12/05/2018
ms.keywords: AUTHZ_ACCESS_CHECK_NO_DEEP_COPY_SD, AuthzAccessCheck, AuthzAccessCheck function [Security], _win32_authzaccesscheck, authz/AuthzAccessCheck, security.authzaccesscheck
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
 - AuthzAccessCheck
 - authz/AuthzAccessCheck
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
 - AuthzAccessCheck
---

# AuthzAccessCheck function


## -description

The <b>AuthzAccessCheck</b> function determines which access bits can be granted to a client for a given set of <a href="/windows/desktop/SecGloss/s-gly">security descriptors</a>. The <a href="/windows/desktop/api/authz/ns-authz-authz_access_reply">AUTHZ_ACCESS_REPLY</a> structure returns an array of granted <a href="/windows/desktop/SecGloss/a-gly">access masks</a> and error status. Optionally, access masks that will always be granted can be cached, and a handle to cached values is returned.

## -parameters

### -param Flags [in]

A <b>DWORD</b> value that specifies how the security descriptor is copied. This parameter can be one of the following values. 

Starting with Windows 8 and Windows Server 2012,  when you call this function on a remote context handle, the upper 16 bits must be zero.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
If <i>phAccessCheckResults</i> is not <b>NULL</b>, a  deep copy of the security descriptor is copied to the handle referenced by <i>phAccessCheckResults</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_ACCESS_CHECK_NO_DEEP_COPY_SD"></a><a id="authz_access_check_no_deep_copy_sd"></a><dl>
<dt><b>AUTHZ_ACCESS_CHECK_NO_DEEP_COPY_SD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A deep copy of the security descriptor is not performed. The calling application must pass the address of an <b>AUTHZ_ACCESS_CHECK_RESULTS_HANDLE</b> handle in <i>phAccessCheckResults</i>. The <b>AuthzAccessCheck</b> function sets this handle to a security descriptor that must remain valid during subsequent calls to <a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a>.

</td>
</tr>
</table>

### -param hAuthzClientContext [in]

A handle to a structure that represents the client.
					

Starting with Windows 8 and Windows Server 2012,  the client context can be local or remote.

### -param pRequest [in]

A pointer to an <a href="/windows/desktop/api/authz/ns-authz-authz_access_request">AUTHZ_ACCESS_REQUEST</a> structure that specifies the desired access mask, principal self <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID), and the object type list structure, if it exists.

### -param hAuditEvent [in, optional]

A structure that contains object-specific audit information. When the value of this parameter is not <b>null</b>, an audit is automatically requested. Static audit information is read from the resource manager structure. 

Starting with Windows 8 and Windows Server 2012,  when you use this function with a remote context handle, the value of the parameter must be <b>NULL</b>.

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure to be used for access checks. The owner SID for the object is picked from this security descriptor. A <b>NULL </b><a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) in this security descriptor represents a <b>NULL</b> DACL for the entire object. Make sure the security descriptor contains OWNER and DACL information, or an error code 87 or "invalid parameter" message will be generated.

<div class="alert"><b>Important</b>  <b>NULL</b> DACLs permit all types of access to all users; therefore, do not use <b>NULL</b> DACLs. For information about creating a DACL, see <a href="/windows/desktop/SecBP/creating-a-dacl">Creating a DACL</a>.</div>
<div> </div>
 A <b>NULL </b><a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) in this security descriptor is treated the same way as an empty SACL.

### -param OptionalSecurityDescriptorArray [in, optional]

An array of <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structures. <b>NULL </b><a href="/windows/desktop/SecGloss/a-gly">access control lists</a> (ACLs) in these security descriptors are treated as empty ACLs. The ACL for the entire object is the logical concatenation of all of the ACLs.

### -param OptionalSecurityDescriptorCount [in, optional]

The number of security descriptors not including the primary security descriptor.

### -param pReply [in, out]

A pointer to an 
<a href="/windows/desktop/api/authz/ns-authz-authz_access_reply">AUTHZ_ACCESS_REPLY</a> structure that contains the results of the access check. Before calling the <b>AuthzAccessCheck</b> function, an application must allocate memory for the <b>GrantedAccessMask</b> and <b>SaclEvaluationResults</b> members of the <b>AUTHZ_ACCESS_REPLY</b> structure referenced by <i>pReply</i>.

### -param phAccessCheckResults [out, optional]

A pointer to return a handle to the cached results of the access check. When this parameter value is not <b>null</b>, the results of this access check call will be cached. This results in a MAXIMUM_ALLOWED check. 

Starting with Windows 8 and Windows Server 2012,  when you use this function with a remote context handle, the value of the parameter must be <b>NULL</b>.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> callback function will be called if the DACL of the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure pointed to by the <i>pSecurityDescriptor</i> parameter contains a callback <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).

Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown. For more information, see the <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language-for-conditional-aces-">Security Descriptor Definition Language for Conditional ACEs</a> topic.

For more information, see the <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a> and <a href="/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a> overviews.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_access_reply">AUTHZ_ACCESS_REPLY</a>



<a href="/windows/desktop/api/authz/ns-authz-authz_access_request">AUTHZ_ACCESS_REQUEST</a>



<a href="/windows/desktop/api/authz/nf-authz-authzcachedaccesscheck">AuthzCachedAccessCheck</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a>



<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How AccessCheck Works</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language-for-conditional-aces-">Security Descriptor Definition Language for Conditional ACEs</a>