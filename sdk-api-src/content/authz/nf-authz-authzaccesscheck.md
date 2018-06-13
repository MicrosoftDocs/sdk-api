---
UID: NF:authz.AuthzAccessCheck
title: AuthzAccessCheck function
author: windows-sdk-content
description: Determines which access bits can be granted to a client for a given set of security descriptors.
old-location: security\authzaccesscheck.htm
old-project: SecAuthZ
ms.assetid: 633c2a73-169c-4e0c-abb6-96c360bd63cf
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AUTHZ_ACCESS_CHECK_NO_DEEP_COPY_SD, AuthzAccessCheck, AuthzAccessCheck function [Security], _win32_authzaccesscheck, authz/AuthzAccessCheck, security.authzaccesscheck
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzAccessCheck
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzAccessCheck function


## -description


The <b>AuthzAccessCheck</b> function determines which access bits can be granted to a client for a given set of <a href="https://msdn.microsoft.com/library/windows/hardware/ff563698">security descriptors</a>. The <a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a> structure returns an array of granted <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access masks</a> and error status. Optionally, access masks that will always be granted can be cached, and a handle to cached values is returned.


## -parameters




### -param Flags

TBD


### -param hAuthzClientContext [in]

A handle to a structure that represents the client.
					

Starting with Windows 8 and Windows Server 2012,  the client context can be local or remote.


### -param pRequest [in]

A pointer to an <a href="https://msdn.microsoft.com/3748075c-b31a-4669-b8a6-1a540449d8fa">AUTHZ_ACCESS_REQUEST</a> structure that specifies the desired access mask, principal self <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID), and the object type list structure, if it exists.


### -param hAuditEvent

TBD


### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure to be used for access checks. The owner SID for the object is picked from this security descriptor. A <b>NULL </b><a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) in this security descriptor represents a <b>NULL</b> DACL for the entire object. Make sure the security descriptor contains OWNER and DACL information, or an error code 87 or "invalid parameter" message will be generated.

<div class="alert"><b>Important</b>  <b>NULL</b> DACLs permit all types of access to all users; therefore, do not use <b>NULL</b> DACLs. For information about creating a DACL, see <a href="https://msdn.microsoft.com/f8ec202f-4f34-4123-8f3c-cfc5960b4dc2">Creating a DACL</a>.</div>
<div> </div>
 A <b>NULL </b><a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) in this security descriptor is treated the same way as an empty SACL.
					


### -param OptionalSecurityDescriptorArray [in, optional]

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structures. <b>NULL </b><a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control lists</a> (ACLs) in these security descriptors are treated as empty ACLs. The ACL for the entire object is the logical concatenation of all of the ACLs.
					


### -param OptionalSecurityDescriptorCount [in, optional]

The number of security descriptors not including the primary security descriptor.
					


### -param pReply [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a> structure that contains the results of the access check. Before calling the <b>AuthzAccessCheck</b> function, an application must allocate memory for the <b>GrantedAccessMask</b> and <b>SaclEvaluationResults</b> members of the <b>AUTHZ_ACCESS_REPLY</b> structure referenced by <i>pReply</i>.


### -param phAccessCheckResults [out, optional]

A pointer to return a handle to the cached results of the access check. When this parameter value is not <b>null</b>, the results of this access check call will be cached. This results in a MAXIMUM_ALLOWED check. 

Starting with Windows 8 and Windows Server 2012,  when you use this function with a remote context handle, the value of the parameter must be <b>NULL</b>.


#### - AuditEvent [in, optional]

A structure that contains object-specific audit information. When the value of this parameter is not <b>null</b>, an audit is automatically requested. Static audit information is read from the resource manager structure. 

Starting with Windows 8 and Windows Server 2012,  when you use this function with a remote context handle, the value of the parameter must be <b>NULL</b>.


#### - flags [in]

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
A deep copy of the security descriptor is not performed. The calling application must pass the address of an <b>AUTHZ_ACCESS_CHECK_RESULTS_HANDLE</b> handle in <i>phAccessCheckResults</i>. The <b>AuthzAccessCheck</b> function sets this handle to a security descriptor that must remain valid during subsequent calls to <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a>.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/e8a510e6-0739-4765-ad07-3bcb1b9c905c">AuthzAccessCheckCallback</a> callback function will be called if the DACL of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure pointed to by the <i>pSecurityDescriptor</i> parameter contains a callback <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE).

Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown. For more information, see the <a href="https://msdn.microsoft.com/cdc3629d-c4d8-4910-8838-3bdb601f7064">Security Descriptor Definition Language for Conditional ACEs</a> topic.

For more information, see the <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a> and <a href="https://msdn.microsoft.com/5A06B8D8-F14B-4D9E-9ED6-4246A26BF945">Centralized Authorization Policy</a> overviews.




## -see-also




<a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a>



<a href="https://msdn.microsoft.com/3748075c-b31a-4669-b8a6-1a540449d8fa">AUTHZ_ACCESS_REQUEST</a>



<a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a>



<a href="https://www.bing.com/search?q=Basic+Access+Control+Functions">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/5A06B8D8-F14B-4D9E-9ED6-4246A26BF945">Centralized Authorization Policy</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/cdc3629d-c4d8-4910-8838-3bdb601f7064">Security Descriptor Definition Language for Conditional ACEs</a>
 

 

