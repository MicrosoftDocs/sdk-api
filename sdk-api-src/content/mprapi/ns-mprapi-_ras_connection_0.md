---
UID: NS:mprapi._RAS_CONNECTION_0
title: "_RAS_CONNECTION_0"
author: windows-sdk-content
description: The RAS_CONNECTION_0 structure contains general information regarding a specific connection, such as user name or domain. For more detailed information about a specific connection, such as bytes sent or received, see RAS_CONNECTION_1.
old-location: rras\ras_connection_0.htm
tech.root: RRAS
ms.assetid: e2561365-be3f-44cd-bb3c-18b001fc4d5d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PRAS_CONNECTION_0, PRAS_CONNECTION_0, PRAS_CONNECTION_0 structure pointer [RAS], RAS_CONNECTION_0, RAS_CONNECTION_0 structure [RAS], RAS_FLAGS_ARAP_CONNECTION, RAS_FLAGS_DORMANT, RAS_FLAGS_IKEV2_CONNECTION, RAS_FLAGS_MESSENGER_PRESENT, RAS_FLAGS_PPP_CONNECTION, RAS_FLAGS_QUARANTINE_PRESENT, _RAS_CONNECTION_0, _mpr_ras_connection_0, mprapi/PRAS_CONNECTION_0, mprapi/RAS_CONNECTION_0, rras.ras_connection_0"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - RAS_CONNECTION_0
product: Windows
targetos: Windows
req.typenames: RAS_CONNECTION_0, *PRAS_CONNECTION_0
req.redist: 
---

# _RAS_CONNECTION_0 structure


## -description


The 
<b>RAS_CONNECTION_0</b> structure contains general information regarding a specific connection, such as user name or domain. For more detailed information about a specific connection, such as bytes sent or received, see 
<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>.


## -struct-fields




### -field hConnection

A handle to the connection.


### -field hInterface

A handle to the interface.


### -field dwConnectDuration

A value that represent the duration of the connection, in seconds.


### -field dwInterfaceType

A <a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">ROUTER_INTERFACE_TYPE</a> enumeration that identifies the type of connection interface.


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
The messenger service is active on the client and messages can be sent to the client using <a href="https://msdn.microsoft.com/3c0d8b6c-25c1-47c3-baef-d82e6d2fa52f">MprAdminSendUserMessage</a>.



</td>
</tr>
<tr>
<td width="40%"><a id="RAS_FLAGS_QUARANTINE_PRESENT"></a><a id="ras_flags_quarantine_present"></a><dl>
<dt><b>RAS_FLAGS_QUARANTINE_PRESENT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The connection is currently in quarantine. For information on how to remove the connection from quarantine, please see <a href="https://msdn.microsoft.com/9d8c33b4-4227-4538-bc0e-f663d1d560f1">MprAdminConnectionRemoveQuarantine</a>.

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




<a href="https://msdn.microsoft.com/58fea0ca-b7c1-4d32-bcfc-10b41e101f30">MprAdminAcceptReauthentication</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/8c31d345-8f57-47f5-a021-e399f7ccca5d">MprAdminConnectionHangupNotification3</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS
		  Administration Structures</a>



<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>



<a href="https://msdn.microsoft.com/5dcc20f0-7447-4256-9dde-18a4a3c95816">RAS_CONNECTION_2</a>



<a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

