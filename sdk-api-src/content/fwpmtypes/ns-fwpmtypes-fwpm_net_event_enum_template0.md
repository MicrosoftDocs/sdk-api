---
UID: NS:fwpmtypes.FWPM_NET_EVENT_ENUM_TEMPLATE0_
title: FWPM_NET_EVENT_ENUM_TEMPLATE0 (fwpmtypes.h)
description: Used for enumerating net events.
helpviewer_keywords: ["FWPM_CONDITION_ALE_APP_ID","FWPM_CONDITION_ALE_USER_ID","FWPM_CONDITION_IP_LOCAL_ADDRESS","FWPM_CONDITION_IP_LOCAL_PORT","FWPM_CONDITION_IP_PROTOCOL","FWPM_CONDITION_IP_REMOTE_ADDRESS","FWPM_CONDITION_IP_REMOTE_PORT","FWPM_CONDITION_SCOPE_ID","FWPM_NET_EVENT_ENUM_TEMPLATE0","FWPM_NET_EVENT_ENUM_TEMPLATE0 structure [Filtering]","fwp.fwpm_net_event_enum_template0","fwpmtypes/FWPM_NET_EVENT_ENUM_TEMPLATE0"]
old-location: fwp\fwpm_net_event_enum_template0.htm
tech.root: fwp
ms.assetid: 79711b24-e092-4a36-810a-6acad279eb90
ms.date: 05/02/2024
ms.keywords: FWPM_CONDITION_ALE_APP_ID, FWPM_CONDITION_ALE_USER_ID, FWPM_CONDITION_IP_LOCAL_ADDRESS, FWPM_CONDITION_IP_LOCAL_PORT, FWPM_CONDITION_IP_PROTOCOL, FWPM_CONDITION_IP_REMOTE_ADDRESS, FWPM_CONDITION_IP_REMOTE_PORT, FWPM_CONDITION_SCOPE_ID, FWPM_NET_EVENT_ENUM_TEMPLATE0, FWPM_NET_EVENT_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_net_event_enum_template0, fwpmtypes/FWPM_NET_EVENT_ENUM_TEMPLATE0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_NET_EVENT_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_ENUM_TEMPLATE0_
 - fwpmtypes/FWPM_NET_EVENT_ENUM_TEMPLATE0_
 - FWPM_NET_EVENT_ENUM_TEMPLATE0
 - fwpmtypes/FWPM_NET_EVENT_ENUM_TEMPLATE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_ENUM_TEMPLATE0
---

## -description

The <b>FWPM_NET_EVENT_ENUM_TEMPLATE0</b> structure is used for enumerating net events.

## -struct-fields

### -field startTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the start time of the period to be checked for net events.

### -field endTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the end time of the period to be checked for net events. It must be greater than or equal to <b>startTime</b>.

### -field numFilterConditions

Indicates the number of filter conditions in the <b>filterCondition</b> member.  If this field is 0, all events will be returned.

### -field filterCondition

An array of [FWPM_FILTER_CONDITION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0) structures that contain distinct filter conditions (duplicated filter conditions will generate an error). All conditions must be true for the action to be
   performed. In other words, the conditions are AND'ed together. If no
   conditions are specified, the action is always performed. 


Supported filtering conditions.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONDITION_IP_PROTOCOL"></a><a id="fwpm_condition_ip_protocol"></a><dl>
<dt><b>FWPM_CONDITION_IP_PROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
The IP protocol number, as specified in RFC 1700.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></a><a id="fwpm_condition_ip_local_address"></a><dl>
<dt><b>FWPM_CONDITION_IP_LOCAL_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The local IP address.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></a><a id="fwpm_condition_ip_remote_address"></a><dl>
<dt><b>FWPM_CONDITION_IP_REMOTE_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The remote IP address.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONDITION_IP_LOCAL_PORT"></a><a id="fwpm_condition_ip_local_port"></a><dl>
<dt><b>FWPM_CONDITION_IP_LOCAL_PORT</b></dt>
</dl>
</td>
<td width="60%">
The local transport protocol port number. For ICMP, the message type.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONDITION_IP_REMOTE_PORT"></a><a id="fwpm_condition_ip_remote_port"></a><dl>
<dt><b>FWPM_CONDITION_IP_REMOTE_PORT</b></dt>
</dl>
</td>
<td width="60%">
The remote transport protocol port number. For ICMP, the  message code.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONDITION_SCOPE_ID"></a><a id="fwpm_condition_scope_id"></a><dl>
<dt><b>FWPM_CONDITION_SCOPE_ID</b></dt>
</dl>
</td>
<td width="60%">
The interface IPv6 scope identifier. Reserved for internal use.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CONDITION_ALE_APP_ID"></a><a id="fwpm_condition_ale_app_id"></a><dl>
<dt><b>FWPM_CONDITION_ALE_APP_ID</b></dt>
</dl>
</td>
<td width="60%">
The full path of the application.
</td>
</tr>

<tr>
<td width="40%"><a id="FWPM_CONDITION_ALE_USER_ID"></a><a id="fwpm_condition_ale_user_id"></a><dl>
<dt><b>FWPM_CONDITION_ALE_USER_ID</b></dt>
</dl>
</td>
<td width="60%">
The identification of the local user.
</td>
</tr>

<tr>
<td width="40%"><a id="FWPM_CONDITION_NET_EVENT_TYPE"></a><a id="fwpm_condition_net_event_type"></a><dl>
<dt><b>FWPM_CONDITION_NET_EVENT_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The 32-bit event type to be notified of, as defined in the <a href="/windows/win32/api/fwpmtypes/ne-fwpmtypes-fwpm_net_event_type">FWPM_NET_EVENT_TYPE</a> enumeration.
</td>
</tr>

</table>

## -remarks

<b>FWPM_NET_EVENT_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_NET_EVENT_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_FILTER_CONDITION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)



<a href="/windows/desktop/FWP/filtering-condition-identifiers-">Filtering Condition Identifiers</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>