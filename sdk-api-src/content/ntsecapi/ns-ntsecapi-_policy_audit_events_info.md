---
UID: NS:ntsecapi._POLICY_AUDIT_EVENTS_INFO
title: "_POLICY_AUDIT_EVENTS_INFO"
author: windows-driver-content
description: The POLICY_AUDIT_EVENTS_INFO structure is used to set and query the system's auditing rules.
old-location: security\policy_audit_events_info.htm
old-project: SecMgmt
ms.assetid: 3442e5e5-78cf-4bda-ba11-0f51ee40df16
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PPOLICY_AUDIT_EVENTS_INFO, POLICY_AUDIT_EVENTS_INFO, POLICY_AUDIT_EVENTS_INFO structure [Security], POLICY_AUDIT_EVENT_FAILURE, POLICY_AUDIT_EVENT_NONE, POLICY_AUDIT_EVENT_SUCCESS, POLICY_AUDIT_EVENT_UNCHANGED, PPOLICY_AUDIT_EVENTS_INFO, PPOLICY_AUDIT_EVENTS_INFO structure pointer [Security], _POLICY_AUDIT_EVENTS_INFO, _lsa_policy_audit_events_info, ntsecapi/POLICY_AUDIT_EVENTS_INFO, ntsecapi/PPOLICY_AUDIT_EVENTS_INFO, security.policy_audit_events_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: POLICY_AUDIT_EVENTS_INFO, *PPOLICY_AUDIT_EVENTS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	POLICY_AUDIT_EVENTS_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _POLICY_AUDIT_EVENTS_INFO structure


## -description


The <b>POLICY_AUDIT_EVENTS_INFO</b> structure is used to set and query the system's auditing rules. The 
<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a> and 
<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyAuditEventsInformation</b>.


## -struct-fields




### -field AuditingMode

Indicates whether auditing is enabled. 




If this flag is <b>TRUE</b>, the system generates audit records according to the event auditing options specified in the <b>EventAuditingOptions</b> member.

If this flag is <b>FALSE</b>, the system does not generate audit records. However, note that set operations update the event auditing options as specified in the <b>EventAuditingOptions</b> member even when <b>AuditingMode</b> is <b>FALSE</b>.


### -field EventAuditingOptions

Pointer to an array of POLICY_AUDIT_EVENT_OPTIONS variables. Each element in this array specifies the auditing options for an audit event type. The index of each array element corresponds to an audit event type value in the 
<a href="https://msdn.microsoft.com/e8dbd1d5-37d5-4a97-9d1c-c645871dc7a5">POLICY_AUDIT_EVENT_TYPE</a> enumeration type. 




Each POLICY_AUDIT_EVENT_OPTIONS variable in the array can specify the following auditing options. You can also combine the success and failure options, POLICY_AUDIT_EVENT_SUCCESS and POLICY_AUDIT_EVENT_FAILURE.

When <a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LSASetInformationPolicy</a> is called to change the audit policy, any new POLICY_AUDIT_EVENT_OPTIONS array elements are added to any existing audit options. Adding a new POLICY_AUDIT_EVENT_OPTIONS element combined with the POLICY_AUDIT_EVENT_NONE audit option cancels all previous audit options and begins a new set of options.

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




<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/e8dbd1d5-37d5-4a97-9d1c-c645871dc7a5">POLICY_AUDIT_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a>
 

 

