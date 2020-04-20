---
UID: NS:lmserver._SERVER_TRANSPORT_INFO_3
title: SERVER_TRANSPORT_INFO_3 (lmserver.h)
description: The SERVER_TRANSPORT_INFO_3 structure contains information about the specified transport protocol, including name, address and password (credentials). This information level is valid only for the NetServerTransportAddEx function.helpviewer_keywords: ["*LPSERVER_TRANSPORT_INFO_3","*PSERVER_TRANSPORT_INFO_3","LPSERVER_TRANSPORT_INFO_3","LPSERVER_TRANSPORT_INFO_3 structure pointer [Network Management]","PSERVER_TRANSPORT_INFO_3","PSERVER_TRANSPORT_INFO_3 structure pointer [Network Management]","SERVER_TRANSPORT_INFO_3","SERVER_TRANSPORT_INFO_3 structure [Network Management]","SVTI2_REMAP_PIPE_NAMES","SVTI2_SCOPED_NAME","_win32_server_transport_info_3_str","lmserver/LPSERVER_TRANSPORT_INFO_3","lmserver/PSERVER_TRANSPORT_INFO_3","lmserver/SERVER_TRANSPORT_INFO_3","netmgmt.server_transport_info_3_str"]
old-location: netmgmt\server_transport_info_3_str.htm
tech.root: NetMgmt
ms.assetid: 045d60d4-518f-4ce4-b611-e23d1588d5d3
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_TRANSPORT_INFO_3, *PSERVER_TRANSPORT_INFO_3, LPSERVER_TRANSPORT_INFO_3, LPSERVER_TRANSPORT_INFO_3 structure pointer [Network Management], PSERVER_TRANSPORT_INFO_3, PSERVER_TRANSPORT_INFO_3 structure pointer [Network Management], SERVER_TRANSPORT_INFO_3, SERVER_TRANSPORT_INFO_3 structure [Network Management], SVTI2_REMAP_PIPE_NAMES, SVTI2_SCOPED_NAME, _win32_server_transport_info_3_str, lmserver/LPSERVER_TRANSPORT_INFO_3, lmserver/PSERVER_TRANSPORT_INFO_3, lmserver/SERVER_TRANSPORT_INFO_3, netmgmt.server_transport_info_3_str'
f1_keywords:
- lmserver/SERVER_TRANSPORT_INFO_3
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Lmserver.h
api_name:
- SERVER_TRANSPORT_INFO_3
targetos: Windows
req.typenames: SERVER_TRANSPORT_INFO_3, *PSERVER_TRANSPORT_INFO_3, *LPSERVER_TRANSPORT_INFO_3
req.redist: 
ms.custom: 19H1
---

# SERVER_TRANSPORT_INFO_3 structure


## -description


The 
				<b>SERVER_TRANSPORT_INFO_3</b> structure contains information about the specified transport protocol, including name, address and password (credentials). This information level is valid only for the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.


## -struct-fields




### -field svti3_numberofvcs

Type: <b>DWORD</b>

The number of clients connected to the server that are using the transport protocol specified by the <b>svti3_transportname</b> member.


### -field svti3_transportname

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the name of a transport device; for example,

<pre class="syntax" xml:space="preserve"><code>\Device\NetBT_Tcpip_{2C9725F4-151A-11D3-AEEC-C3B211BD350B}
</code></pre>
This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field svti3_transportaddress

Type: <b>LPBYTE</b>

A pointer to a variable that contains the address the server is using on the transport device specified by the <b>svti3_transportname</b> member.

This member is usually the NetBIOS name that the server is using. In these instances, the name must be 16 characters long, and the last character must be a blank character (0x20).


### -field svti3_transportaddress.size_is

 


### -field svti3_transportaddress.size_is.svti3_transportaddresslength

 


### -field svti3_transportaddresslength

Type: <b>DWORD</b>

The length, in bytes, of the <b>svti3_transportaddress</b> member. For NetBIOS names, the value of this member is 16 (decimal).


### -field svti3_networkaddress

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the address the network adapter is using. The string is transport-specific.

You can retrieve this value only with a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a> function. You cannot set this value with a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a> function or the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field svti3_domain

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the name of the domain to which the server should announce its presence. (When you call 
<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>, this member is the name of the domain to which the server is announcing its presence.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field svti3_flags

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
 


### -field svti3_passwordlength

Type: <b>DWORD</b>

The number of valid bytes in the <b>svti3_password</b> member.


### -field svti3_password

Type: <b>BYTE[256]</b>

The credentials to use for the new transport address. If the <b>svti3_passwordlength</b> member is zero, the credentials for the server are used.


## -remarks



The 
				<b>SERVER_TRANSPORT_INFO_3</b> structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function to bind the specified server to the transport protocol.

An example of the use of the SVTI2_REMAP_PIPE_NAMES value follows. Call the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function to add a transport to the server, specifying the address of "MyServer" in the <b>svti3_transportaddress</b> member, and <b>SVTI2_REMAP_PIPE_NAMES</b> in the <b>svti3_flags</b> member. When a client attempts to open "Pipe" on "\\MyServer" the client will actually open $$MyServer\Pipe instead.

The <b>svti3_passwordlength</b> and <b>svti3_password</b> members are necessary for a client and server to perform mutual authentication.

On Windows Server 2008  and Windows Vista with SP1, every name registered with the Windows remote file server (SRV) is designated as either a scoped name or a non-scoped name.  Every share that is added to the system will then either be attached to all of the non-scoped names, or to a single scoped name.  Applications that wish to use the scoping features are responsible for both registering the new name as a scoped endpoint and then creating the shares with an appropriate scope. In this way, legacy uses of the Network Management and Network Share Management functions are not affected in any way since they continue to register shares and names as non-scoped names.  

A scoped endpoint is created by calling the <a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function with the <i>level</i> parameter set to 2 and the <i>bufptr</i> parameter pointed to a <a href="https://docs.microsoft.com/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti2_flags</b> member. A scoped endpoint is also created by calling the <b>NetServerTransportAddEx</b> function with the <i>level</i> parameter set to 3 and the <i>bufptr</i> parameter pointed to a <b>SERVER_TRANSPORT_INFO_3</b> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti3_flags</b> member. 

When the <b>SVTI2_SCOPED_NAME</b> bit value is set for a transport, then shares can be added with a corresponding server name (the <b>shi503_servername</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure) in a scoped fashion using the <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a> function.  If there is no transport registered with the <b>SVTI2_SCOPED_NAME</b> bit value and the name provided in <b>shi503_servername</b> member, then the share add in a scoped fashion will not succeed.


The <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a> function is used to add a scoped share on a remote server specified in the <i>servername</i> parameter. The remote server specified in the <b>shi503_servername</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> passed in the <i>bufptr</i> parameter must have been bound to a transport protocol using the <a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function as a scoped endpoint. The <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <b>shi503_servername</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> or <b>SERVER_TRANSPORT_INFO_3</b> structure for the transport protocol.  The <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a> function is used to delete a scoped share.  The <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> and <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a> functions are to used to get and set information on a scoped share.  

Scoped endpoints are generally used by the cluster namespace.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportdel">NetServerTransportDel</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>
 

 

