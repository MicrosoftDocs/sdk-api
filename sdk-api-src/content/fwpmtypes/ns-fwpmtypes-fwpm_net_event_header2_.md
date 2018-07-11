---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER2_
title: FWPM_NET_EVENT_HEADER2_
author: windows-sdk-content
description: Contains information common to all events.
old-location: fwp\fwpm_net_event_header2.htm
old-project: fwp
ms.assetid: 1120d807-9188-4674-9acd-4b96e680f8af
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET, FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER2, FWPM_NET_EVENT_HEADER2 structure [Filtering], FWPM_NET_EVENT_HEADER2_, fwp.fwpm_net_event_header2, fwpmtypes/FWPM_NET_EVENT_HEADER2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_NET_EVENT_HEADER2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_HEADER2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_HEADER2_ structure


## -description


The <b>FWPM_NET_EVENT_HEADER2</b> structure contains information common to all events.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_HEADER2</b> is the specific implementation of FWPM_NET_EVENT_HEADER available for Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista and Windows 7, <a href="https://msdn.microsoft.com/2fbb805d-d38b-4918-a291-fe1000ac2ea2">FWPM_NET_EVENT_HEADER0</a> is available.</div><div> </div>

## -struct-fields




### -field timeStamp

Type: <b>FILETIME</b>

Time that the event occurred.


### -field flags

Type: <b>UINT32</b>

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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a></b>

The IP version being used. 


### -field ipProtocol

Type: <b>UINT8</b>

The IP protocol specified as an IPPROTO value. See the <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> reference topic for more information on possible protocol values.


### -field localAddrV4

Type: <b>UINT32</b>

The IPv4 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field localAddrV6

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a></b>

The IPv6 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field remoteAddrV4

Type: <b>UINT32</b>

The IPv4 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field remoteAddrV6

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a></b>

The IPv6 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field localPort

Type: <b>UINT16</b>

The local port.


### -field remotePort

Type: <b>UINT16</b>

The remote port.


### -field scopeId

Type: <b>UINT32</b>

The IPv6 scope ID.


### -field appId

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a></b>

The application ID of the local application associated with the event.


### -field userId

Type: <b>SID*</b>

The user ID corresponding to the traffic.


### -field addressFamily

Type: <b><a href="https://msdn.microsoft.com/358305a6-e0a6-4d01-92be-fd88b3bd32a0">FWP_AF</a></b>

A superset of non-Internet protocols.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_NONE</b>.


### -field packageSid

Type: <b>SID*</b>

The security identifier (SID) representing the package identifier (also referred to as the app container SID) intending to send or receive the network traffic.


## -see-also




<a href="https://msdn.microsoft.com/358305a6-e0a6-4d01-92be-fd88b3bd32a0">FWP_AF</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>
 

 

