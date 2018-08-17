---
UID: NS:authz._AUTHZ_ACCESS_REPLY
title: "_AUTHZ_ACCESS_REPLY"
author: windows-sdk-content
description: Defines an access check reply.
old-location: security\authz_access_reply.htm
old-project: secauthz
ms.assetid: 7162bf80-3730-46d7-a603-2a55b969c9ba
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PAUTHZ_ACCESS_REPLY, AUTHZ_ACCESS_REPLY, AUTHZ_ACCESS_REPLY structure [Security], AUTHZ_GENERATE_FAILURE_AUDIT, AUTHZ_GENERATE_SUCCESS_AUDIT, ERROR_ACCESS_DENIED, ERROR_PRIVILEGE_NOT_HELD, ERROR_SUCCESS, PAUTHZ_ACCESS_REPLY, PAUTHZ_ACCESS_REPLY structure pointer [Security], _AUTHZ_ACCESS_REPLY, _win32_authz_access_reply, authz/AUTHZ_ACCESS_REPLY, authz/PAUTHZ_ACCESS_REPLY, security.authz_access_reply"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: authz.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
req.typenames: AUTHZ_ACCESS_REPLY, *PAUTHZ_ACCESS_REPLY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_ACCESS_REPLY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _AUTHZ_ACCESS_REPLY structure


## -description


The <b>AUTHZ_ACCESS_REPLY</b> structure defines an access check reply.


## -struct-fields




### -field ResultListLength

The number of elements in the <b>GrantedAccessMask</b>, <b>SaclEvaluationResults</b>, and <b>Error</b> arrays. This number matches the number of entries in the object type list structure used in the access check.
						 If no object type is used to represent the object, then set <b>ResultListLength</b> to one.


### -field GrantedAccessMask

An array of granted access masks. Memory for this array is allocated by the application before calling <a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>.


### -field SaclEvaluationResults

An array of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) evaluation results. Memory for this array is allocated by the application before calling <a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>. SACL evaluation will only be performed if auditing is requested. Each element of this member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_GENERATE_SUCCESS_AUDIT"></a><a id="authz_generate_success_audit"></a><dl>
<dt><b>AUTHZ_GENERATE_SUCCESS_AUDIT</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
An audit message that indicates success was generated.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_GENERATE_FAILURE_AUDIT"></a><a id="authz_generate_failure_audit"></a><dl>
<dt><b>AUTHZ_GENERATE_FAILURE_AUDIT</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
An audit message that indicates failure was generated.

</td>
</tr>
</table>
 


### -field Error

An array of results for each element of the array. Memory for this array is allocated by the application before calling <a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>. 




The following table lists the possible error values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ERROR_SUCCESS"></a><a id="error_success"></a><dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
All the access bits, not including MAXIMUM_ALLOWED, are granted and the <b>GrantedAccessMask</b> member is not zero.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_PRIVILEGE_NOT_HELD"></a><a id="error_privilege_not_held"></a><dl>
<dt><b>ERROR_PRIVILEGE_NOT_HELD</b></dt>
</dl>
</td>
<td width="60%">
DesiredAccess includes ACCESS_SYSTEM_SECURITY and the client does not have SeSecurityPrivilege.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_ACCESS_DENIED"></a><a id="error_access_denied"></a><dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Includes each of the following: 




<ul>
<li>The requested bits are not granted.</li>
<li>MaximumAllowed bit is on and granted access is zero.</li>
<li>DesiredAccess is zero.</li>
</ul>
</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>
 

 

