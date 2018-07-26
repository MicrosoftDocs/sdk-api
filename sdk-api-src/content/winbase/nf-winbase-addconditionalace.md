---
UID: NF:winbase.AddConditionalAce
title: AddConditionalAce function
author: windows-sdk-content
description: Adds a conditional access control entry (ACE) to the specified access control list (ACL).
old-location: security\addconditionalace.htm
old-project: secauthz
ms.assetid: 89f038be-d15c-4c0b-8145-ba531bdf87ce
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: ACCESS_ALLOWED_CALLBACK_ACE_TYPE, ACCESS_DENIED_CALLBACK_ACE_TYPE, AddConditionalAce, AddConditionalAce function [Security], CONTAINER_INHERIT_ACE, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, SYSTEM_AUDIT_CALLBACK_ACE_TYPE, security.addconditionalace, winbase/AddConditionalAce
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - AddConditionalAce
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# AddConditionalAce function


## -description


The <b>AddConditionalAce</b> function adds a conditional  <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) to the specified <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). A conditional ACE specifies a logical condition that is evaluated during access checks.


## -parameters




### -param pAcl [in, out]

A pointer to an 
ACL. This function adds an ACE to this ACL.

The value of this parameter cannot be <b>NULL</b>.


### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. This value can be ACL_REVISION or ACL_REVISION_DS. 
      Use ACL_REVISION_DS if the ACL contains object-specific ACEs.


### -param AceFlags [in]

A set of bit flags that control ACE inheritance. The function sets these flags in the <b>AceFlags</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure of the new ACE. This parameter can be a combination of the following values.

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
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object to which the ACL is assigned, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs while not changing ACEs that were directly applied to the object.

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
</table>
 


### -param AceType [in]

The type of the ACE.

This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_CALLBACK_ACE_TYPE"></a><a id="access_allowed_callback_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_CALLBACK_ACE_TYPE</b></dt>
<dt>0x9</dt>
</dl>
</td>
<td width="60%">
Access-allowed callback ACE that uses the 
<a href="https://msdn.microsoft.com/0dbca19b-4b54-4c55-920a-c00335692d68">ACCESS_ALLOWED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_CALLBACK_ACE_TYPE"></a><a id="access_denied_callback_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_CALLBACK_ACE_TYPE</b></dt>
<dt>0xA</dt>
</dl>
</td>
<td width="60%">
Access-denied callback ACE that uses the 
<a href="https://msdn.microsoft.com/6df77b27-7aa3-455f-bffe-eeb90ba1bc15">ACCESS_DENIED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_CALLBACK_ACE_TYPE"></a><a id="system_audit_callback_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_CALLBACK_ACE_TYPE</b></dt>
<dt>0xD</dt>
</dl>
</td>
<td width="60%">
System audit callback ACE that uses the 
<a href="https://msdn.microsoft.com/4d1799b0-3e55-48d7-94ff-c0094945adea">SYSTEM_AUDIT_CALLBACK_ACE</a> structure.

</td>
</tr>
</table>
 


### -param AccessMask [in]

Specifies the mask of access rights to be granted to the specified SID.


### -param pSid [in]

A pointer to the 
SID  that represents a user, group, or logon account being granted access.


### -param ConditionStr [in]

A string that specifies the conditional statement to be evaluated for the ACE.


### -param ReturnLength [out]

The size, in bytes, of the ACL. If the buffer specified by the <i>pACL</i> parameter is not of sufficient size, the value of this parameter is the required size.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the <i>pAcl</i> buffer.

</td>
</tr>
</table>
 



