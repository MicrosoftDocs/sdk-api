---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _AUDIT_POLICY_INFORMATION structure


## -description


The <b>AUDIT_POLICY_INFORMATION</b> structure specifies a security event type and when to audit that type.


## -struct-fields




### -field AuditSubCategoryGuid

A <b>GUID</b> structure that specifies an audit subcategory.


### -field AuditingInformation

A set of bit flags that specify the conditions under which  the security event type specified by the <b>AuditSubCategoryGuid</b> and <b>AuditCategoryGuid</b> members are audited. The following values are defined.

<div class="alert"><b>Important</b>  Note that the meaning of these values differs depending on which function is using this structure.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_UNCHANGED"></a><a id="policy_audit_event_unchanged"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_UNCHANGED</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Do not change auditing options for the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a">AuditSetSystemPolicy</a> and <a href="https://msdn.microsoft.com/5c268033-65fd-4a74-90a1-4b9e1e18daf1">AuditQuerySystemPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_SUCCESS"></a><a id="policy_audit_event_success"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_SUCCESS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Audit successful occurrences of the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a">AuditSetSystemPolicy</a> and <a href="https://msdn.microsoft.com/5c268033-65fd-4a74-90a1-4b9e1e18daf1">AuditQuerySystemPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_FAILURE"></a><a id="policy_audit_event_failure"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_FAILURE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Audit failed attempts to cause the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a">AuditSetSystemPolicy</a> and <a href="https://msdn.microsoft.com/5c268033-65fd-4a74-90a1-4b9e1e18daf1">AuditQuerySystemPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_NONE"></a><a id="policy_audit_event_none"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_NONE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Do not audit the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a">AuditSetSystemPolicy</a> and <a href="https://msdn.microsoft.com/5c268033-65fd-4a74-90a1-4b9e1e18daf1">AuditQuerySystemPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="PER_USER_POLICY_UNCHANGED"></a><a id="per_user_policy_unchanged"></a><dl>
<dt><b>PER_USER_POLICY_UNCHANGED</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Do not change auditing options for the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a> and <a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="PER_USER_AUDIT_SUCCESS_INCLUDE"></a><a id="per_user_audit_success_include"></a><dl>
<dt><b>PER_USER_AUDIT_SUCCESS_INCLUDE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Audit successful occurrences of the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a> and <a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="PER_USER_AUDIT_SUCCESS_EXCLUDE"></a><a id="per_user_audit_success_exclude"></a><dl>
<dt><b>PER_USER_AUDIT_SUCCESS_EXCLUDE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Do not audit successful occurrences of the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a> and <a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="PER_USER_AUDIT_FAILURE_INCLUDE"></a><a id="per_user_audit_failure_include"></a><dl>
<dt><b>PER_USER_AUDIT_FAILURE_INCLUDE</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Audit failed attempts to cause the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a> and <a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="PER_USER_AUDIT_FAILURE_EXCLUDE"></a><a id="per_user_audit_failure_exclude"></a><dl>
<dt><b>PER_USER_AUDIT_FAILURE_EXCLUDE</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Do not audit failed attempts to cause the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a> and <a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="PER_USER_AUDIT_NONE"></a><a id="per_user_audit_none"></a><dl>
<dt><b>PER_USER_AUDIT_NONE</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Do not audit the specified event type.

This value is valid for the <a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a> and <a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a> functions.

</td>
</tr>
</table>
 


### -field AuditCategoryGuid

A <b>GUID</b> structure that specifies an audit-policy category.


## -see-also




<a href="https://msdn.microsoft.com/cac928e5-8d8f-4b2f-9c1b-c00dc891e3d1">AuditComputeEffectivePolicyBySid</a>



<a href="https://msdn.microsoft.com/e5fc9b8d-a61e-48c2-9093-f27167232cc8">AuditComputeEffectivePolicyByToken</a>



<a href="https://msdn.microsoft.com/7d4790de-ebd6-4840-b532-7158b8d80db2">AuditQueryPerUserPolicy</a>



<a href="https://msdn.microsoft.com/5c268033-65fd-4a74-90a1-4b9e1e18daf1">AuditQuerySystemPolicy</a>



<a href="https://msdn.microsoft.com/a6cef640-5658-4c13-96fb-a664d2a61b57">AuditSetPerUserPolicy</a>



<a href="https://msdn.microsoft.com/9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a">AuditSetSystemPolicy</a>
 

 

