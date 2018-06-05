---
UID: NF:authz.AuthzInitializeResourceManagerEx
title: AuthzInitializeResourceManagerEx function
author: windows-sdk-content
description: Allocates and initializes a resource manager structure.
old-location: security\authzinitializeresourcemanagerex.htm
old-project: SecAuthZ
ms.assetid: CDB78606-1B53-4516-90E6-1FF096B3D7D9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AUTHZ_RM_FLAG_INITIALIZE_UNDER_IMPERSONATION, AUTHZ_RM_FLAG_NO_AUDIT, AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES, AuthzInitializeResourceManagerEx, AuthzInitializeResourceManagerEx function [Security], authz/AuthzInitializeResourceManagerEx, security.authzinitializeresourcemanagerex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Authz.dll
api_name:
-	AuthzInitializeResourceManagerEx
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzInitializeResourceManagerEx function


## -description


The <b>AuthzInitializeResourceManagerEx</b> function initializes an Authz resource manager and returns a handle to it. Use this function rather than <a href="https://msdn.microsoft.com/e3f6b37d-2c33-4b17-97b4-762bf55561c5">AuthzInitializeResourceManager</a> when you want the resource manager to manage Central Access Policies (CAPs).


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

A pointer to a <a href="https://msdn.microsoft.com/30489BE7-5B95-413E-8134-039AD3220A50">AUTHZ_INIT_INFO</a> structure that contains the authorization resource manager initialization information.


### -param phAuthzResourceManager [out]

A pointer to the returned resource manager handle. When you have finished using the handle, free it by using the <a href="https://msdn.microsoft.com/8b716368-8d81-4c62-9086-0976b39bbcf8">AuthzFreeResourceManager</a> function.


## -returns




						If the function succeeds, the function returns a value of <b>TRUE</b>. 

If the function fails, it returns a value of <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is specified, then <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> and <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a> ignore CAPID (Central Access Policie ID) <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a><a href="https://msdn.microsoft.com/library/windows/hardware/hh406640">SYSTEM_SCOPED_POLICY_ID_ACE</a> and will not evaluate CAPs.

If the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is not specified and pfnGetCentralAccessPolicy is <b>NULL</b>, then <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> and <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a> will get CAPs from LSA. For more information, see <a href="https://msdn.microsoft.com/DF10F5CE-BBF5-4CA8-919B-F59B7775C983">LsaGetAppliedCAPIDs</a>.

If the AUTHZ_RM_FLAG_NO_CENTRAL_ACCESS_POLICIES flag is not specified and a central access policy callback is provided by the resource manager, then <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> and <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a> will get CAPs from the resource manager by invoking the callback.

The LSA and the central access policy callback can indicate that CAPs are not supported, in which case <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> and <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a> ignore CAPID ACEs and will not evaluate CAPs.

The LSA and the central access policy callback may fail to return a CAP that corresponds to a particular CAPID, in which case <b>AuthzAccessCheck</b> and <b>AuthzCachedAccessCheck</b> use the same default CAP as the kernel AccessCheck.





## -see-also




<a href="https://msdn.microsoft.com/DF10F5CE-BBF5-4CA8-919B-F59B7775C983">LsaGetAppliedCAPIDs</a>
 

 

