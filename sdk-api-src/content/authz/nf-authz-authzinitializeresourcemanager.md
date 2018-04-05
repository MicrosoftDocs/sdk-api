---
UID: NF:authz.AuthzInitializeResourceManager
title: AuthzInitializeResourceManager function
author: windows-driver-content
description: Uses Authz to verify that clients have access to various resources.
old-location: security\authzinitializeresourcemanager.htm
old-project: SecAuthZ
ms.assetid: e3f6b37d-2c33-4b17-97b4-762bf55561c5
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION, AUTHZ_RM_FLAG_NO_AUDIT, AUTHZ_RM_FLAG_NO_CENTRALIZED_ACCESS_POLICIES, AuthzInitializeResourceManager, AuthzInitializeResourceManager function [Security], _win32_authzinitializeresourcemanager, authz/AuthzInitializeResourceManager, security.authzinitializeresourcemanager
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Authz.dll
-	Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
-	AuthzInitializeResourceManager
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzInitializeResourceManager function


## -description



			The <b>AuthzInitializeResourceManager</b> function uses Authz to verify that clients have access to various resources.


## -parameters




### -param Flags

TBD


### -param pfnDynamicAccessCheck

TBD


### -param pfnComputeDynamicGroups [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/c20a02a0-5303-4433-a484-5a89999b32b9">AuthzComputeGroupsCallback</a> callback function called by the resource manager during initialization of an <i>AuthzClientContext</i> handle. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.


### -param pfnFreeDynamicGroups [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/5563311c-2bd1-4e96-ba0a-5a4225050f77">AuthzFreeGroupsCallback</a> callback function called by the resource manager to free <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) attribute arrays allocated by the compute dynamic groups callback. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.


### -param szResourceManagerName [in]

A string that identifies the resource manager. This parameter can be <b>NULL</b> if the resource manager does not need a name.


### -param phAuthzResourceManager [out]

A pointer to the returned resource manager handle. When you have finished using the handle, free it by calling the <a href="https://msdn.microsoft.com/8b716368-8d81-4c62-9086-0976b39bbcf8">AuthzFreeResourceManager</a> function.


#### - flags [in]

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
<td width="40%"><a id="AUTHZ_RM_FLAG_NO_CENTRALIZED_ACCESS_POLICIES"></a><a id="authz_rm_flag_no_centralized_access_policies"></a><dl>
<dt><b>AUTHZ_RM_FLAG_NO_CENTRALIZED_ACCESS_POLICIES</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The resource manager ignores CAP IDs and does not evaluate centralized access policies.

</td>
</tr>
</table>
 

AUTHZ_RM_FLAG_NO_AUDIT and AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION can be bitwise-combined.


#### - pfnAccessCheck [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/e8a510e6-0739-4765-ad07-3bcb1b9c905c">AuthzAccessCheckCallback</a> callback function that the resource manager calls each time it encounters a callback
						<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) during <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) evaluation in 
<a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> or 
<a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a>.  This parameter can be <b>NULL</b> if no access check callback function is used.


## -returns




						If the function succeeds, the function returns a nonzero value. 

If the function fails, it returns a zero value. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a>



<a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a>



<a href="https://msdn.microsoft.com/8b716368-8d81-4c62-9086-0976b39bbcf8">AuthzFreeResourceManager</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

