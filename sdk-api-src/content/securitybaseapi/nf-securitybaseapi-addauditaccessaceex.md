---
UID: NF:securitybaseapi.AddAuditAccessAceEx
title: AddAuditAccessAceEx function
author: windows-sdk-content
description: Adds a system-audit access control entry (ACE) to the end of a system access control list (SACL).
old-location: security\addauditaccessaceex.htm
tech.root: SecAuthZ
ms.assetid: ddd1d815-c4ce-4572-982c-139e17cda192
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddAuditAccessAceEx, AddAuditAccessAceEx function [Security], CONTAINER_INHERIT_ACE, FAILED_ACCESS_ACE_FLAG, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, SUCCESSFUL_ACCESS_ACE_FLAG, _win32_addauditaccessaceex, security.addauditaccessaceex, securitybaseapi/AddAuditAccessAceEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AddAuditAccessAceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddAuditAccessAceEx function


## -description


The <b>AddAuditAccessAceEx</b> function adds a system-audit <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) to the end of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL).


## -parameters




### -param pAcl [in, out]

A pointer to a SACL. The <b>AddAuditAccessAceEx</b> function adds a system-audit ACE to this SACL. The ACE is in the form of a 
<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a> structure.


### -param dwAceRevision [in]

Specifies the revision level of the SACL being modified. This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the SACL contains object-specific ACEs.


### -param AceFlags [in]

A set of bit flags that control ACE inheritance and the type of access attempts to audit. The function sets these flags in the <b>AceFlags</b> member of the <a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure of the new ACE. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by container objects.

</td>
</tr>
<tr>
<td width="40%"><a id="FAILED_ACCESS_ACE_FLAG"></a><a id="failed_access_ace_flag"></a><dl>
<dt><b>FAILED_ACCESS_ACE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If you set this flag or specify <b>TRUE</b> for the <i>bAuditFailure</i> parameter, failed attempts to use the specified access rights cause the system to generate an audit record in the security event log.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object to which the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) is assigned, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs, while not changing ACEs that were directly applied to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE bits are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by noncontainer objects.

</td>
</tr>
<tr>
<td width="40%"><a id="SUCCESSFUL_ACCESS_ACE_FLAG"></a><a id="successful_access_ace_flag"></a><dl>
<dt><b>SUCCESSFUL_ACCESS_ACE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If you set this flag or specify <b>TRUE</b> for the <i>bAuditSuccess</i> parameter, successful uses of the specified access rights cause the system to generate an audit record in the security event log.

</td>
</tr>
</table>
 


### -param dwAccessMask [in]

A set of bit flags that use the 
<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> format to specify the access rights that the new ACE audits for the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


### -param pSid [in]

A pointer to a 
SID that identifies the user, group, or <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> for which the new ACE audits access.


### -param bAuditSuccess [in]

Specifies whether successful uses of the specified access rights cause the system to generate an audit record in the security event log. If this flag is <b>TRUE</b> or if the <i>AceFlags</i> parameter specifies the SUCCESSFUL_ACCESS_ACE_FLAG flag, the system records successful access attempts; otherwise, it does not.


### -param bAuditFailure [in]

Specifies whether failed attempts to use the specified access rights cause the system to generate an audit record in the security event log. If this flag is <b>TRUE</b> or if the <i>AceFlags</i> parameter specifies the FAILED_ACCESS_ACE_FLAG flag, the system records failed access attempts; otherwise, it does not.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALLOTTED_SPACE_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the ACL. A larger ACL buffer is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ACL</b></dt>
</dl>
</td>
<td width="60%">
The specified ACL is not properly formed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>AceFlags</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The specified SID is not structurally valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The specified revision is not known or is incompatible with that of the ACL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The ACE was successfully added.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/6ddec01f-237f-4b6a-8ea8-a126017b30c5">AddAccessAllowedAceEx</a>



<a href="https://msdn.microsoft.com/e353c88c-f82e-40c0-b676-38f0060acc81">AddAccessDeniedAceEx</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a>
 

 

