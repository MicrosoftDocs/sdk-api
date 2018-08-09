---
UID: NF:authz.AuthzCachedAccessCheck
title: AuthzCachedAccessCheck function
author: windows-sdk-content
description: Performs a fast access check based on a cached handle containing the static granted bits from a previous AuthzAccessCheck call.
old-location: security\authzcachedaccesscheck.htm
old-project: secauthz
ms.assetid: 8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AuthzCachedAccessCheck, AuthzCachedAccessCheck function [Security], _win32_authzcachedaccesscheck, authz/AuthzCachedAccessCheck, security.authzcachedaccesscheck
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
 - AuthzCachedAccessCheck
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzCachedAccessCheck function


## -description


The <b>AuthzCachedAccessCheck</b> function performs a fast access check based on a cached handle containing the static granted bits from a previous 
<a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> call.


## -parameters




### -param Flags [in]

Reserved for future use.


### -param hAccessCheckResults [in]

A handle to the cached access check results.


### -param pRequest [in]

Access request handle specifying the desired <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a>, principal self <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>, and the object type list structure (if any).


### -param hAuditEvent [in]

A structure that contains object-specific audit information. When the value of this parameter is not null, an audit is automatically requested. Static audit information is read from the resource manager structure.


### -param pReply [out]

A pointer to an 
<a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a> handle that returns the results of access check as an array of GrantedAccessMask/ErrorValue pairs. The number of pairs returned is supplied by the caller in the <b>ResultListLength</b> member of the <b>AUTHZ_ACCESS_REPLY</b> structure.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
Pointers to the primary <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> and the optional security descriptor array are stored in <i>AuthzHandle</i> at the time of handle creation. These pointers must still be valid. 

The <b>AuthzCachedAccessCheck</b> function maintains a cache as a result of evaluating Central Access Policies (CAP) on objects unless CAPs are ignored, for example when the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is used. The client may call the <a href="https://msdn.microsoft.com/0F972A95-3CD7-4C86-99DE-5B3D50CE9A34">AuthzFreeCentralAccessPolicyCache</a> function to free up this cache. Note that this requires a subsequent call to <b>AuthzCachedAccessCheck</b> to rebuild the cache if necessary. 

For more information, see the <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a> and <a href="https://msdn.microsoft.com/5A06B8D8-F14B-4D9E-9ED6-4246A26BF945">Centralized Authorization Policy</a> overviews.




## -see-also




<a href="https://msdn.microsoft.com/7162bf80-3730-46d7-a603-2a55b969c9ba">AUTHZ_ACCESS_REPLY</a>



<a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a>



<a href="https://msdn.microsoft.com/0F972A95-3CD7-4C86-99DE-5B3D50CE9A34">AuthzFreeCentralAccessPolicyCache</a>



<a href="https://msdn.microsoft.com/e3f6b37d-2c33-4b17-97b4-762bf55561c5">AuthzInitializeResourceManager</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/5A06B8D8-F14B-4D9E-9ED6-4246A26BF945">Centralized Authorization Policy</a>



<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How AccessCheck Works</a>
 

 

