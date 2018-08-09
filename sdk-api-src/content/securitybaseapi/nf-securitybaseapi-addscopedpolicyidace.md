---
UID: NF:securitybaseapi.AddScopedPolicyIDAce
title: AddScopedPolicyIDAce function
author: windows-sdk-content
description: Adds a SYSTEM_SCOPED_POLICY_ID_ACEaccess control entry (ACE) to the end of a system access control list (SACL).
old-location: security\addscopedpolicyidace.htm
old-project: secauthz
ms.assetid: 30AA5730-566C-4B02-A904-5A38237EE8E3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddScopedPolicyIDAce, AddScopedPolicyIDAce function [Security], CONTAINER_INHERIT_ACE, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, security.addscopedpolicyidace, securitybaseapi/AddScopedPolicyIDAce
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
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
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AddScopedPolicyIDAce
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# AddScopedPolicyIDAce function


## -description


The <b>AddScopedPolicyIDAce</b> function adds a <a href="https://msdn.microsoft.com/library/windows/hardware/hh406640">SYSTEM_SCOPED_POLICY_ID_ACE</a> <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) to the end of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL). A <b>SYSTEM_SCOPED_POLICY_ID_ACE</b> structure specifies a central access policy (CAP) to be associated with the resource and can be  used during access checks. The set of standard access rights are defined in the <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a> topic.


## -parameters




### -param pAcl [in, out]

A pointer to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). This function adds an ACE to this ACL. The value of this parameter cannot be <b>NULL</b>.


### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs.


### -param AceFlags [in]

A set of bit flags that control ACE inheritance. The function sets these flags in the <b>AceFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure of the new ACE.

For consistency with the Windows 8 Advanced File Permissions UI, applications should specify the CONTAINER_INHERIT_ACE and OBJECT_INHERIT_ACE flags in the <i>AceFlags</i> parameter.


This parameter can be a combination of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by the container objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object the ACE is assigned to, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs while not changing ACEs that were directly applied to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE bits are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by non-container objects.

</td>
</tr>
</table>
 


### -param AccessMask [in]

Must be zero for Windows 8 and Windows Server 2012.


### -param pSid [in]

A pointer to the SID (S-1-17-*) that identifies the Central Access Policy to be associated with the resource.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>
 

 

