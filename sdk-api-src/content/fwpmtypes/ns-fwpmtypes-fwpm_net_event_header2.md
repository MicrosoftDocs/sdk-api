---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER2_
title: FWPM_NET_EVENT_HEADER2 (fwpmtypes.h)
description: Contains information common to all events.
helpviewer_keywords: ["FWPM_NET_EVENT_FLAG_APP_ID_SET","FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET","FWPM_NET_EVENT_FLAG_IP_VERSION_SET","FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET","FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET","FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET","FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET","FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET","FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET","FWPM_NET_EVENT_FLAG_SCOPE_ID_SET","FWPM_NET_EVENT_FLAG_USER_ID_SET","FWPM_NET_EVENT_HEADER2","FWPM_NET_EVENT_HEADER2 structure [Filtering]","fwp.fwpm_net_event_header2","fwpmtypes/FWPM_NET_EVENT_HEADER2"]
old-location: fwp\fwpm_net_event_header2.htm
tech.root: fwp
ms.assetid: 1120d807-9188-4674-9acd-4b96e680f8af
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET, FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER2, FWPM_NET_EVENT_HEADER2 structure [Filtering], fwp.fwpm_net_event_header2, fwpmtypes/FWPM_NET_EVENT_HEADER2
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_NET_EVENT_HEADER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_HEADER2_
 - fwpmtypes/FWPM_NET_EVENT_HEADER2_
 - FWPM_NET_EVENT_HEADER2
 - fwpmtypes/FWPM_NET_EVENT_HEADER2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_HEADER2
---

# FWPM_NET_EVENT_HEADER2 structure


## -description

The <b>FWPM_NET_EVENT_HEADER2</b> structure contains information common to all events.
[FWPM_NET_EVENT_HEADER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) is available.</div><div> </div>

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

Type: [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)</b>

The IP version being used.

### -field ipProtocol

Type: <b>UINT8</b>

The IP protocol specified as an IPPROTO value. See the <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> reference topic for more information on possible protocol values.

### -field localAddrV4

Type: <b>UINT32</b>

The IPv4 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field localAddrV6

Type: [FWP_BYTE_ARRAY16](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)</b>

The IPv6 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.

### -field remoteAddrV4

Type: <b>UINT32</b>

The IPv4 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field remoteAddrV6

Type: [FWP_BYTE_ARRAY16](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)</b>

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

Type: [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)</b>

The application ID of the local application associated with the event.

### -field userId

Type: <b>SID*</b>

The user ID corresponding to the traffic.

### -field addressFamily

Type: [FWP_AF](../fwptypes/ne-fwptypes-fwp_af.md)</b>

A superset of non-Internet protocols.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_NONE</b>.

### -field packageSid

Type: <b>SID*</b>

The security identifier (SID) representing the package identifier (also referred to as the app container SID) intending to send or receive the network traffic.

## -see-also

[FWP_AF](../fwptypes/ne-fwptypes-fwp_af.md)



[FWP_BYTE_ARRAY16](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)



[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)