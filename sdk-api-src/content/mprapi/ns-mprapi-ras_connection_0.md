---
UID: NS:mprapi._RAS_CONNECTION_0
title: RAS_CONNECTION_0 (mprapi.h)
description: The RAS_CONNECTION_0 structure contains general information regarding a specific connection, such as user name or domain. For more detailed information about a specific connection, such as bytes sent or received, see RAS_CONNECTION_1.
helpviewer_keywords: ["*PRAS_CONNECTION_0","PRAS_CONNECTION_0","PRAS_CONNECTION_0 structure pointer [RAS]","RAS_CONNECTION_0","RAS_CONNECTION_0 structure [RAS]","RAS_FLAGS_ARAP_CONNECTION","RAS_FLAGS_DORMANT","RAS_FLAGS_IKEV2_CONNECTION","RAS_FLAGS_MESSENGER_PRESENT","RAS_FLAGS_PPP_CONNECTION","RAS_FLAGS_QUARANTINE_PRESENT","_mpr_ras_connection_0","mprapi/PRAS_CONNECTION_0","mprapi/RAS_CONNECTION_0","rras.ras_connection_0"]
old-location: rras\ras_connection_0.htm
tech.root: RRAS
ms.assetid: e2561365-be3f-44cd-bb3c-18b001fc4d5d
ms.date: 12/05/2018
ms.keywords: '*PRAS_CONNECTION_0, PRAS_CONNECTION_0, PRAS_CONNECTION_0 structure pointer [RAS], RAS_CONNECTION_0, RAS_CONNECTION_0 structure [RAS], RAS_FLAGS_ARAP_CONNECTION, RAS_FLAGS_DORMANT, RAS_FLAGS_IKEV2_CONNECTION, RAS_FLAGS_MESSENGER_PRESENT, RAS_FLAGS_PPP_CONNECTION, RAS_FLAGS_QUARANTINE_PRESENT, _mpr_ras_connection_0, mprapi/PRAS_CONNECTION_0, mprapi/RAS_CONNECTION_0, rras.ras_connection_0'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RAS_CONNECTION_0, *PRAS_CONNECTION_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_CONNECTION_0
 - mprapi/_RAS_CONNECTION_0
 - PRAS_CONNECTION_0
 - mprapi/PRAS_CONNECTION_0
 - RAS_CONNECTION_0
 - mprapi/RAS_CONNECTION_0
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
 - RAS_CONNECTION_0
---

# RAS_CONNECTION_0 structure


## -description

The 
<b>RAS_CONNECTION_0</b> structure contains general information regarding a specific connection, such as user name or domain. For more detailed information about a specific connection, such as bytes sent or received, see 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>.

## -struct-fields

### -field hConnection

A handle to the connection.

### -field hInterface

A handle to the interface.

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

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptreauthentication">MprAdminAcceptReauthentication</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification3">MprAdminConnectionHangupNotification3</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS
		  Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>