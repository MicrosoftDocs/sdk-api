---
UID: NS:ntsecapi._AUDIT_POLICY_INFORMATION
title: AUDIT_POLICY_INFORMATION (ntsecapi.h)
description: Specifies a security event type and when to audit that type.
helpviewer_keywords: ["*PAUDIT_POLICY_INFORMATION","AUDIT_POLICY_INFORMATION","AUDIT_POLICY_INFORMATION structure [Security]","PAUDIT_POLICY_INFORMATION","PAUDIT_POLICY_INFORMATION structure pointer [Security]","PER_USER_AUDIT_FAILURE_EXCLUDE","PER_USER_AUDIT_FAILURE_INCLUDE","PER_USER_AUDIT_NONE","PER_USER_AUDIT_SUCCESS_EXCLUDE","PER_USER_AUDIT_SUCCESS_INCLUDE","PER_USER_POLICY_UNCHANGED","POLICY_AUDIT_EVENT_FAILURE","POLICY_AUDIT_EVENT_NONE","POLICY_AUDIT_EVENT_SUCCESS","POLICY_AUDIT_EVENT_UNCHANGED","ntsecapi/AUDIT_POLICY_INFORMATION","ntsecapi/PAUDIT_POLICY_INFORMATION","security.audit_policy_information"]
old-location: security\audit_policy_information.htm
tech.root: security
ms.assetid: 3fafeec9-a028-4a65-933e-fb973eb257b0
ms.date: 12/05/2018
ms.keywords: '*PAUDIT_POLICY_INFORMATION, AUDIT_POLICY_INFORMATION, AUDIT_POLICY_INFORMATION structure [Security], PAUDIT_POLICY_INFORMATION, PAUDIT_POLICY_INFORMATION structure pointer [Security], PER_USER_AUDIT_FAILURE_EXCLUDE, PER_USER_AUDIT_FAILURE_INCLUDE, PER_USER_AUDIT_NONE, PER_USER_AUDIT_SUCCESS_EXCLUDE, PER_USER_AUDIT_SUCCESS_INCLUDE, PER_USER_POLICY_UNCHANGED, POLICY_AUDIT_EVENT_FAILURE, POLICY_AUDIT_EVENT_NONE, POLICY_AUDIT_EVENT_SUCCESS, POLICY_AUDIT_EVENT_UNCHANGED, ntsecapi/AUDIT_POLICY_INFORMATION, ntsecapi/PAUDIT_POLICY_INFORMATION, security.audit_policy_information'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AUDIT_POLICY_INFORMATION, *PAUDIT_POLICY_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUDIT_POLICY_INFORMATION
 - ntsecapi/_AUDIT_POLICY_INFORMATION
 - PAUDIT_POLICY_INFORMATION
 - ntsecapi/PAUDIT_POLICY_INFORMATION
 - AUDIT_POLICY_INFORMATION
 - ntsecapi/AUDIT_POLICY_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - AUDIT_POLICY_INFORMATION
---

# AUDIT_POLICY_INFORMATION structure


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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetsystempolicy">AuditSetSystemPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditquerysystempolicy">AuditQuerySystemPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetsystempolicy">AuditSetSystemPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditquerysystempolicy">AuditQuerySystemPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetsystempolicy">AuditSetSystemPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditquerysystempolicy">AuditQuerySystemPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetsystempolicy">AuditSetSystemPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditquerysystempolicy">AuditQuerySystemPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a> functions.

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

This value is valid for the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a> and <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a> functions.

</td>
</tr>
</table>

### -field AuditCategoryGuid

A <b>GUID</b> structure that specifies an audit-policy category.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditcomputeeffectivepolicybysid">AuditComputeEffectivePolicyBySid</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditcomputeeffectivepolicybytoken">AuditComputeEffectivePolicyByToken</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditquerysystempolicy">AuditQuerySystemPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetsystempolicy">AuditSetSystemPolicy</a>