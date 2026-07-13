---
UID: NS:mprapi._RAS_CONNECTION_EX
title: RAS_CONNECTION_EX (mprapi.h)
description: Contains specific information for the connection that includes:\_the user name, domain, and Globally Unique Identifier (GUID) associated with the connection, its Network Access Protection (NAP) quarantine state, its packet statistics, as well as its Point-to-Point(PPP) and Internet Key Exchange version 2 (IKEv2) related information.
helpviewer_keywords: ["*PRAS_CONNECTION_EX","PRAS_CONNECTION_EX","PRAS_CONNECTION_EX structure pointer [RAS]","RAS_CONNECTION_EX","RAS_CONNECTION_EX structure [RAS]","RAS_FLAGS_ARAP_CONNECTION","RAS_FLAGS_DORMANT","RAS_FLAGS_IKEV2_CONNECTION","RAS_FLAGS_MESSENGER_PRESENT","RAS_FLAGS_PPP_CONNECTION","RAS_FLAGS_QUARANTINE_PRESENT","mprapi/PRAS_CONNECTION_EX","mprapi/RAS_CONNECTION_EX","rras.ras_connection_ex"]
old-location: rras\ras_connection_ex.htm
tech.root: RRAS
ms.assetid: 48526073-caeb-463e-b85b-1ef46ca1e2b4
ms.date: 12/05/2018
ms.keywords: '*PRAS_CONNECTION_EX, PRAS_CONNECTION_EX, PRAS_CONNECTION_EX structure pointer [RAS], RAS_CONNECTION_EX, RAS_CONNECTION_EX structure [RAS], RAS_FLAGS_ARAP_CONNECTION, RAS_FLAGS_DORMANT, RAS_FLAGS_IKEV2_CONNECTION, RAS_FLAGS_MESSENGER_PRESENT, RAS_FLAGS_PPP_CONNECTION, RAS_FLAGS_QUARANTINE_PRESENT, mprapi/PRAS_CONNECTION_EX, mprapi/RAS_CONNECTION_EX, rras.ras_connection_ex'
req.header: mprapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RAS_CONNECTION_EX, *PRAS_CONNECTION_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_CONNECTION_EX
 - mprapi/_RAS_CONNECTION_EX
 - PRAS_CONNECTION_EX
 - mprapi/PRAS_CONNECTION_EX
 - RAS_CONNECTION_EX
 - mprapi/RAS_CONNECTION_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - RAS_CONNECTION_EX
---

# RAS_CONNECTION_EX structure


## -description

The 
<b>RAS_CONNECTION_EX</b> structure contains specific information for the connection that includes: the user name, domain, and  Globally Unique Identifier (GUID) associated with the connection, its Network Access Protection (NAP) quarantine state, its packet statistics, as well as its Point-to-Point(PPP) and Internet Key Exchange version 2 (IKEv2) related information.

The <b>RAS_CONNECTION_EX</b> structure contains most of the same information as the <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>,
			 <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>, <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>, and <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a> combined structures.

## -struct-fields

### -field Header

A <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_object_header">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <b>RAS_CONNECTION_EX</b> structure. 

<div class="alert"><b>Note</b>  The <b>revision</b> member  of  <b>Header</b> must be <b>MPRAPI_RAS_CONNECTION_OBJECT_REVISION_1</b> and <b>type</b> must be <b>MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT</b>.</div>
<div> </div>

### -field dwConnectDuration

A value that represent the duration of the connection, in seconds.

### -field dwInterfaceType

A <a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">ROUTER_INTERFACE_TYPE</a> enumeration that identifies the type of connection interface.

### -field dwConnectionFlags

A bitmap of flags that specify connection attributes. <b>dwConnectionFlags</b> must contain at least one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RAS_FLAGS_PPP_CONNECTION"></a><a id="ras_flags_ppp_connection"></a><dl>
<dt><b>RAS_FLAGS_PPP_CONNECTION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The connection is using Point-to-Point Protocol (PPP).

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_FLAGS_MESSENGER_PRESENT"></a><a id="ras_flags_messenger_present"></a><dl>
<dt><b>RAS_FLAGS_MESSENGER_PRESENT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The messenger service is active on the client and messages can be sent to the client using <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminsendusermessage">MprAdminSendUserMessage</a>.



</td>
</tr>
<tr>
<td width="40%"><a id="RAS_FLAGS_QUARANTINE_PRESENT"></a><a id="ras_flags_quarantine_present"></a><dl>
<dt><b>RAS_FLAGS_QUARANTINE_PRESENT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The connection is currently in quarantine. For information on how to remove the connection from quarantine, please see <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionremovequarantine">MprAdminConnectionRemoveQuarantine</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_FLAGS_ARAP_CONNECTION"></a><a id="ras_flags_arap_connection"></a><dl>
<dt><b>RAS_FLAGS_ARAP_CONNECTION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The connection is using AppleTalk Remote Access Protocol (ARAP).

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_FLAGS_IKEV2_CONNECTION"></a><a id="ras_flags_ikev2_connection"></a><dl>
<dt><b>RAS_FLAGS_IKEV2_CONNECTION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The connection is using IKEv2.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_FLAGS_DORMANT"></a><a id="ras_flags_dormant"></a><dl>
<dt><b>RAS_FLAGS_DORMANT</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The connection is using IKEv2 and the server is not reachable.

</td>
</tr>
</table>

### -field wszInterfaceName

 A null-terminated Unicode string that contains the name of the interface for this connection.

### -field wszUserName

A null-terminated Unicode string that contains the name of the user logged on to the connection.

### -field wszLogonDomain

A null-terminated Unicode string that contains the domain on which the connected user is authenticated.

### -field wszRemoteComputer

A null-terminated Unicode string that contains the name of the remote computer.

### -field guid

A GUID  that identifies the connection. For incoming connections, this GUID is valid only as long as the connection is active.

### -field rasQuarState

A <a href="/windows/desktop/api/mprapi/ne-mprapi-ras_quarantine_state">RAS_QUARANTINE_STATE</a> structure that specifies the NAP quarantine state of the connection.

### -field probationTime

A FILETIME structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped. This value is valid only if <b>rasQuarState</b> has a value of <b>RAS_QUAR_STATE_PROBATION</b>.

### -field dwBytesXmited

A value that specifies the number of bytes transmitted on the connection.

### -field dwBytesRcved

A value that specifies the number of bytes received on the connection.

### -field dwFramesXmited

A value that specifies the number of frames transmitted on the connection.

### -field dwFramesRcved

A value that specifies the number of frames received on the connection.

### -field dwCrcErr

A value that specifies the number of Cyclic Redundancy Check (CRC) errors on the connection.

### -field dwTimeoutErr

A value that specifies the number of time-out errors on the connection.

### -field dwAlignmentErr

A value that specifies the number of alignment errors on the connection.

### -field dwHardwareOverrunErr

A value that specifies the number of hardware overrun errors on the connection.

### -field dwFramingErr

A value that specifies the number of framing errors on the connection.

### -field dwBufferOverrunErr

A value that specifies the number of buffer overrun errors on the connection.

### -field dwCompressionRatioIn

A value that specifies the percentage by which data received on this connection is compressed. <b>dwCompressionRatioIn</b> is the size of the compressed data divided by the size of the same data in an uncompressed state.

### -field dwCompressionRatioOut

A value that specifies the percentage by which data transmitted on this connection is compressed. The ratio is the size of the compressed data divided by the size of the same data in an uncompressed state.

### -field dwNumSwitchOvers

A value that specifies the number of IKEv2 Mobility and Multihoming Protocol (MOBIKE) switches that have occurred on the connection as defined in <a href="https://www.ietf.org/rfc/rfc4555.txt">RFC4555</a>. <b>dwNumSwitchOvers</b> is only valid if <b>dwConnectionFlags</b> is <b>RAS_FLAGS_IKEV2_CONNECTION</b>.

### -field wszRemoteEndpointAddress

A null-terminated Unicode string that contains the IP address of the remote computer in the connection. This string is of the form "a.b.c.d".

### -field wszLocalEndpointAddress

A null-terminated Unicode string that contains the IP address of the local computer in the connection. This string is of the form "a.b.c.d".

### -field ProjectionInfo

A <a href="/windows/desktop/api/mprapi/ns-mprapi-projection_info">PROJECTION_INFO</a> structure that contains either a <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_projection_info">PPP_PROJECTION_INFO</a>  or <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_projection_info">IKEV2_PROJECTION_INFO</a> structure.

### -field hConnection

A handle to the RAS connection.

### -field hInterface

A handle to the RAS connection interface.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>