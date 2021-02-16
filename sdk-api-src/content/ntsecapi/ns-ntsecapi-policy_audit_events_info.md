---
UID: NS:ntsecapi._POLICY_AUDIT_EVENTS_INFO
title: POLICY_AUDIT_EVENTS_INFO (ntsecapi.h)
description: The POLICY_AUDIT_EVENTS_INFO structure is used to set and query the system's auditing rules.
helpviewer_keywords: ["*PPOLICY_AUDIT_EVENTS_INFO","POLICY_AUDIT_EVENTS_INFO","POLICY_AUDIT_EVENTS_INFO structure [Security]","POLICY_AUDIT_EVENT_FAILURE","POLICY_AUDIT_EVENT_NONE","POLICY_AUDIT_EVENT_SUCCESS","POLICY_AUDIT_EVENT_UNCHANGED","PPOLICY_AUDIT_EVENTS_INFO","PPOLICY_AUDIT_EVENTS_INFO structure pointer [Security]","_POLICY_AUDIT_EVENTS_INFO","_lsa_policy_audit_events_info","ntsecapi/POLICY_AUDIT_EVENTS_INFO","ntsecapi/PPOLICY_AUDIT_EVENTS_INFO","security.policy_audit_events_info"]
old-location: security\policy_audit_events_info.htm
tech.root: security
ms.assetid: 3442e5e5-78cf-4bda-ba11-0f51ee40df16
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_AUDIT_EVENTS_INFO, POLICY_AUDIT_EVENTS_INFO, POLICY_AUDIT_EVENTS_INFO structure [Security], POLICY_AUDIT_EVENT_FAILURE, POLICY_AUDIT_EVENT_NONE, POLICY_AUDIT_EVENT_SUCCESS, POLICY_AUDIT_EVENT_UNCHANGED, PPOLICY_AUDIT_EVENTS_INFO, PPOLICY_AUDIT_EVENTS_INFO structure pointer [Security], _POLICY_AUDIT_EVENTS_INFO, _lsa_policy_audit_events_info, ntsecapi/POLICY_AUDIT_EVENTS_INFO, ntsecapi/PPOLICY_AUDIT_EVENTS_INFO, security.policy_audit_events_info'
req.header: ntsecapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: POLICY_AUDIT_EVENTS_INFO, *PPOLICY_AUDIT_EVENTS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_AUDIT_EVENTS_INFO
 - ntsecapi/_POLICY_AUDIT_EVENTS_INFO
 - PPOLICY_AUDIT_EVENTS_INFO
 - ntsecapi/PPOLICY_AUDIT_EVENTS_INFO
 - POLICY_AUDIT_EVENTS_INFO
 - ntsecapi/POLICY_AUDIT_EVENTS_INFO
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
 - POLICY_AUDIT_EVENTS_INFO
---

# POLICY_AUDIT_EVENTS_INFO structure


## -description

The <b>POLICY_AUDIT_EVENTS_INFO</b> structure is used to set and query the system's auditing rules. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyAuditEventsInformation</b>.

## -struct-fields

### -field AuditingMode

Indicates whether auditing is enabled. 




If this flag is <b>TRUE</b>, the system generates audit records according to the event auditing options specified in the <b>EventAuditingOptions</b> member.

If this flag is <b>FALSE</b>, the system does not generate audit records. However, note that set operations update the event auditing options as specified in the <b>EventAuditingOptions</b> member even when <b>AuditingMode</b> is <b>FALSE</b>.

### -field EventAuditingOptions

Pointer to an array of POLICY_AUDIT_EVENT_OPTIONS variables. Each element in this array specifies the auditing options for an audit event type. The index of each array element corresponds to an audit event type value in the 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_audit_event_type">POLICY_AUDIT_EVENT_TYPE</a> enumeration type. 




Each POLICY_AUDIT_EVENT_OPTIONS variable in the array can specify the following auditing options. You can also combine the success and failure options, POLICY_AUDIT_EVENT_SUCCESS and POLICY_AUDIT_EVENT_FAILURE.

When <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LSASetInformationPolicy</a> is called to change the audit policy, any new POLICY_AUDIT_EVENT_OPTIONS array elements are added to any existing audit options. Adding a new POLICY_AUDIT_EVENT_OPTIONS element combined with the POLICY_AUDIT_EVENT_NONE audit option cancels all previous audit options and begins a new set of options.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_UNCHANGED"></a><a id="policy_audit_event_unchanged"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_UNCHANGED</b></dt>
</dl>
</td>
<td width="60%">
For set operations, specify this value to leave the current options unchanged. For read operations, this value means that no audit records for this type are generated. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_SUCCESS"></a><a id="policy_audit_event_success"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
Generate audit records for successful events of this type.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_FAILURE"></a><a id="policy_audit_event_failure"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Generate audit records for failed attempts to cause an event of this type to occur.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_AUDIT_EVENT_NONE"></a><a id="policy_audit_event_none"></a><dl>
<dt><b>POLICY_AUDIT_EVENT_NONE</b></dt>
</dl>
</td>
<td width="60%">
Do not generate audit records for events of this type.

</td>
</tr>
</table>

### -field MaximumAuditEventCount

Specifies the number of elements in the <b>EventAuditingOptions</b> array. For set operations, if this value is less than the number of audit event types supported by the system, the system does not change the auditing options for event types with indexes equal to or higher than the value specified in <b>MaximumAuditEventCount</b>.

## -remarks

LSA Policy defines a mask for the valid event auditing options. The POLICY_AUDIT_EVENT_MASK mask evaluates to <b>TRUE</b> if it is set equal to any of the preceding event auditing options.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_audit_event_type">POLICY_AUDIT_EVENT_TYPE</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a>