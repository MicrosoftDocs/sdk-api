---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER3_
title: FWPM_NET_EVENT_HEADER3_
author: windows-sdk-content
description: Contains information common to all events.
old-location: fwp\fwpm_net_event_header3.htm
old-project: FWP
ms.assetid: 1AAC1649-B9F2-40E6-956B-6179A3E1C112
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET, FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER3, FWPM_NET_EVENT_HEADER3 structure [Filtering], FWPM_NET_EVENT_HEADER3_, fwp.fwpm_net_event_header3, fwpmtypes/FWPM_NET_EVENT_HEADER3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_NET_EVENT_HEADER3
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_NET_EVENT_HEADER3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_HEADER3_ structure


## -description


The <b>FWPM_NET_EVENT_HEADER3</b> structure contains information common to all events.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_HEADER3</b> is the specific implementation of FWPM_NET_EVENT_HEADER available for Windows 10, version 1607. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/1120d807-9188-4674-9acd-4b96e680f8af">FWPM_NET_EVENT_HEADER2</a> is available. For Windows Vista and Windows 7, <a href="https://msdn.microsoft.com/2fbb805d-d38b-4918-a291-fe1000ac2ea2">FWPM_NET_EVENT_HEADER0</a> is available.</div><div> </div>

## -struct-fields




### -field timeStamp

Time that the event occurred.


### -field flags

Flags indicating which of the following members are set.  Unused fields must be zero-initialized.

<table>
<tr>
<th>Net event flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET"></a><a id="fwpm_net_event_flag_ip_protocol_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>ipProtocol</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET"></a><a id="fwpm_net_event_flag_local_addr_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET</b></dt>
</dl>
</td>
<td width="60%">
Either the <b>localAddrV4</b> or <b>localAddrV6</b>  member is set. 

<div class="alert"><b>Note</b>  If this flag is present,  <b>FWPM_NET_EVENT_FLAG_IP_VERSION_SET</b> must also be present.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET"></a><a id="fwpm_net_event_flag_remote_addr_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET</b></dt>
</dl>
</td>
<td width="60%">
Either the <b>remoteAddrV4</b> or <b>remoteAddrV6</b> member is set.

<div class="alert"><b>Note</b>  If this flag is present,  <b>FWPM_NET_EVENT_FLAG_IP_VERSION_SET</b> must also be present.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET"></a><a id="fwpm_net_event_flag_local_port_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>localPort</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET"></a><a id="fwpm_net_event_flag_remote_port_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>remotePort</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_APP_ID_SET"></a><a id="fwpm_net_event_flag_app_id_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_APP_ID_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>appId</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_USER_ID_SET"></a><a id="fwpm_net_event_flag_user_id_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_USER_ID_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>userId</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_SCOPE_ID_SET"></a><a id="fwpm_net_event_flag_scope_id_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_SCOPE_ID_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>scopeId</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_IP_VERSION_SET"></a><a id="fwpm_net_event_flag_ip_version_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_IP_VERSION_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>ipVersion</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET"></a><a id="fwpm_net_event_flag_reauth_reason_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET</b></dt>
</dl>
</td>
<td width="60%">
Indicates an existing connection was reauthorized.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET"></a><a id="fwpm_net_event_flag_package_id_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>packageSid</b> member is set.

</td>
</tr>
</table>
 


### -field ipVersion

The IP version being used. 


### -field ipProtocol

The IP protocol specified as an IPPROTO value. See the <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> reference topic for more information on possible protocol values.


### -field localAddrV4

The IPv4 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field localAddrV6

The IPv6 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field remoteAddrV4

The IPv4 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field remoteAddrV6

The IPv6 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field localPort

The local port.


### -field remotePort

The remote port.


### -field scopeId

The IPv6 scope ID.


### -field appId

The application ID of the local application associated with the event.


### -field userId

The user ID corresponding to the traffic.


### -field addressFamily

A superset of non-Internet protocols.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_NONE</b>.


### -field packageSid

The security identifier (SID) representing the package identifier (also referred to as the app container SID) intending to send or receive the network traffic.


### -field enterpriseId

The enterprise identifier for use with enterprise data protection (EDP).


### -field policyFlags

The policy flags for EDP.


### -field effectiveName

The EDP remote server used for name-based policy.


## -see-also




<a href="https://msdn.microsoft.com/358305a6-e0a6-4d01-92be-fd88b3bd32a0">FWP_AF</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>
 

 

