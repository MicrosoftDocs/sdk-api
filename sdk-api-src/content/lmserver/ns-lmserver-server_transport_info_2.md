---
UID: NS:lmserver._SERVER_TRANSPORT_INFO_2
title: SERVER_TRANSPORT_INFO_2 (lmserver.h)
description: The SERVER_TRANSPORT_INFO_2 structure contains information about the specified transport protocol, including the transport name and address. This information level is valid only for the NetServerTransportAddEx function.
helpviewer_keywords: ["*LPSERVER_TRANSPORT_INFO_2","*PSERVER_TRANSPORT_INFO_2","LPSERVER_TRANSPORT_INFO_2","LPSERVER_TRANSPORT_INFO_2 structure pointer [Network Management]","PSERVER_TRANSPORT_INFO_2","PSERVER_TRANSPORT_INFO_2 structure pointer [Network Management]","SERVER_TRANSPORT_INFO_2","SERVER_TRANSPORT_INFO_2 structure [Network Management]","SVTI2_REMAP_PIPE_NAMES","SVTI2_SCOPED_NAME","_win32_server_transport_info_2_str","lmserver/LPSERVER_TRANSPORT_INFO_2","lmserver/PSERVER_TRANSPORT_INFO_2","lmserver/SERVER_TRANSPORT_INFO_2","netmgmt.server_transport_info_2_str"]
old-location: netmgmt\server_transport_info_2_str.htm
tech.root: NetMgmt
ms.assetid: b422eb71-1f93-432d-8283-81432edfe568
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_TRANSPORT_INFO_2, *PSERVER_TRANSPORT_INFO_2, LPSERVER_TRANSPORT_INFO_2, LPSERVER_TRANSPORT_INFO_2 structure pointer [Network Management], PSERVER_TRANSPORT_INFO_2, PSERVER_TRANSPORT_INFO_2 structure pointer [Network Management], SERVER_TRANSPORT_INFO_2, SERVER_TRANSPORT_INFO_2 structure [Network Management], SVTI2_REMAP_PIPE_NAMES, SVTI2_SCOPED_NAME, _win32_server_transport_info_2_str, lmserver/LPSERVER_TRANSPORT_INFO_2, lmserver/PSERVER_TRANSPORT_INFO_2, lmserver/SERVER_TRANSPORT_INFO_2, netmgmt.server_transport_info_2_str'
req.header: lmserver.h
req.include-header: Lm.h
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
req.typenames: SERVER_TRANSPORT_INFO_2, *PSERVER_TRANSPORT_INFO_2, *LPSERVER_TRANSPORT_INFO_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_TRANSPORT_INFO_2
 - lmserver/_SERVER_TRANSPORT_INFO_2
 - PSERVER_TRANSPORT_INFO_2
 - lmserver/PSERVER_TRANSPORT_INFO_2
 - SERVER_TRANSPORT_INFO_2
 - lmserver/SERVER_TRANSPORT_INFO_2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_TRANSPORT_INFO_2
---

# SERVER_TRANSPORT_INFO_2 structure


## -description

The 
				<b>SERVER_TRANSPORT_INFO_2</b> structure contains information about the specified transport protocol, including the transport name and address. This information level is valid only for the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.

## -struct-fields

### -field svti2_numberofvcs

Type: <b>DWORD</b>

The number of clients connected to the server that are using the transport protocol specified by the <b>svti2_transportname</b> member.

### -field svti2_transportname

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the name of a transport device; for example,


``` syntax
\Device\NetBT_Tcpip_{2C9725F4-151A-11D3-AEEC-C3B211BD350B}

```

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field svti2_transportaddress

Type: <b>LPBYTE</b>

A pointer to a variable that contains the address the server is using on the transport device specified by the <b>svti2_transportname</b> member.

This member is usually the NetBIOS name that the server is using. In these instances, the name must be 16 characters long, and the last character must be a blank character (0x20).

### -field svti2_transportaddress.size_is

### -field svti2_transportaddress.size_is.svti2_transportaddresslength

### -field svti2_transportaddresslength

Type: <b>DWORD</b>

The length, in bytes, of the <b>svti2_transportaddress</b> member. For NetBIOS names, the value of this member is 16 (decimal).

### -field svti2_networkaddress

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the address the network adapter is using. The string is transport-specific.

You can retrieve this value only with a call to the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a> function. You cannot set this value with a call to the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a> function or the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field svti2_domain

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the name of the domain to which the server should announce its presence. (When you call 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>, this member is the name of the domain to which the server is announcing its presence.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field svti2_flags

Type: <b>ULONG</b>

This member can be a combination of the following bit values defined in the <i>Lmserver.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SVTI2_REMAP_PIPE_NAMES"></a><a id="svti2_remap_pipe_names"></a><dl>
<dt><b>SVTI2_REMAP_PIPE_NAMES</b></dt>
</dl>
</td>
<td width="60%">
If this value is set for an endpoint, client requests arriving over the transport to open a named pipe are rerouted (remapped) to the following local pipe name:

<b>$$\ServerName\PipeName</b>

For more information on the use of this value, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="SVTI2_SCOPED_NAME"></a><a id="svti2_scoped_name"></a><dl>
<dt><b>SVTI2_SCOPED_NAME</b></dt>
</dl>
</td>
<td width="60%">
If this value is set for an endpoint and there is an attempt to create a second transport with the same network address but a different transport name and conflicting settings for the SCOPED flag, this transport creation will fail.  Thus, every registered transport for a given network address must have the same scoped setting.

For more information on the use of this value, see the Remarks section.

This value is defined on Windows Server 2008  and Windows Vista with SP1.

</td>
</tr>
</table>

## -remarks

The 
				<b>SERVER_TRANSPORT_INFO_2</b> structure is used by the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function to bind the specified server to the transport protocol.

An example of the use of the SVTI2_REMAP_PIPE_NAMES value follows. Call the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function to add a transport to the server, specifying the address of "MyServer" in the <b>svti2_transportaddress</b> member, and <b>SVTI2_REMAP_PIPE_NAMES</b> in the <b>svti2_flags</b> member. When a client attempts to open "Pipe" on "\\MyServer" the client will actually open $$MyServer\Pipe instead.

On Windows Server 2008  and Windows Vista with SP1, every name registered with the Windows remote file server (SRV) is designated as either a scoped name or a non-scoped name.  Every share that is added to the system will then either be attached to all of the non-scoped names, or to a single scoped name.  Applications that wish to use the scoping features are responsible for both registering the new name as a scoped endpoint and then creating the shares with an appropriate scope. In this way, legacy uses of the Network Management and Network Share Management functions are not affected in any way since they continue to register shares and names as non-scoped names.  

A scoped endpoint is created by calling the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function with the <i>level</i> parameter set to 2 and the <i>bufptr</i> parameter pointed to a <b>SERVER_TRANSPORT_INFO_2</b> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti2_flags</b> member. A scoped endpoint is also created by calling the <b>NetServerTransportAddEx</b> function with the <i>level</i> parameter set to 3 and the <i>bufptr</i> parameter pointed to a <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti3_flags</b> member. 

When the <b>SVTI2_SCOPED_NAME</b> bit value is set for a transport, then shares can be added with a corresponding server name (the <b>shi503_servername</b> member of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure) in a scoped fashion using the <a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a> function.  If there is no transport registered with the <b>SVTI2_SCOPED_NAME</b> bit value and the name provided in <b>shi503_servername</b> member, then the share add in a scoped fashion will not succeed.


The <a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a> function is used to add a scoped share on a remote server specified in the <i>servername</i> parameter. The remote server specified in the <b>shi503_servername</b> member of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> passed in the <i>bufptr</i> parameter must have been bound to a transport protocol using the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function as a scoped endpoint. The <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <b>shi503_servername</b> member of the <b>SERVER_TRANSPORT_INFO_2</b> or <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> structure for the transport protocol.  The <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a> function is used to delete a scoped share.  The <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a> functions are to used to get and set information on a scoped share.  

Scoped endpoints are generally used by the cluster namespace.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernameadd">NetServerComputerNameAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernamedel">NetServerComputerNameDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportdel">NetServerTransportDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a>



<a href="/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>
