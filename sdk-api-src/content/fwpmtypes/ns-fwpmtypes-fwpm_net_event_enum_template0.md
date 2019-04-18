---
UID: NS:fwpmtypes.FWPM_NET_EVENT_ENUM_TEMPLATE0_
title: FWPM_NET_EVENT_ENUM_TEMPLATE0 (fwpmtypes.h)
author: windows-sdk-content
description: Used for enumerating net events.
old-location: fwp\fwpm_net_event_enum_template0.htm
tech.root: fwp
ms.assetid: 79711b24-e092-4a36-810a-6acad279eb90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_CONDITION_ALE_APP_ID, FWPM_CONDITION_ALE_USER_ID, FWPM_CONDITION_IP_LOCAL_ADDRESS, FWPM_CONDITION_IP_LOCAL_PORT, FWPM_CONDITION_IP_PROTOCOL, FWPM_CONDITION_IP_REMOTE_ADDRESS, FWPM_CONDITION_IP_REMOTE_PORT, FWPM_CONDITION_SCOPE_ID, FWPM_NET_EVENT_ENUM_TEMPLATE0, FWPM_NET_EVENT_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_net_event_enum_template0, fwpmtypes/FWPM_NET_EVENT_ENUM_TEMPLATE0
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_ENUM_TEMPLATE0
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT_ENUM_TEMPLATE0 structure


## -description


The <b>FWPM_NET_EVENT_ENUM_TEMPLATE0</b> structure is used for enumerating net events.


## -struct-fields




### -field startTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies the start time of the period to be checked for net events.


### -field endTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies the end time of the period to be checked for net events. It must be greater than or equal to <b>startTime</b>.


### -field numFilterConditions

Indicates the number of filter conditions in the <b>filterCondition</b> member.  If this field is 0, all events will be returned.


### -field filterCondition

An array of <a href="https://msdn.microsoft.com/4dfed9d7-e51b-425c-9f27-014229c140be">FWPM_FILTER_CONDITION0</a> structures that contain distinct filter conditions (duplicated filter conditions will generate an error). All conditions must be true for the action to be
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
</table>
 


## -remarks



<b>FWPM_NET_EVENT_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_NET_EVENT_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/4dfed9d7-e51b-425c-9f27-014229c140be">FWPM_FILTER_CONDITION0</a>



<a href="https://msdn.microsoft.com/4f0b970a-e511-4107-8023-22a8775905b9">Filtering Condition Identifiers</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

