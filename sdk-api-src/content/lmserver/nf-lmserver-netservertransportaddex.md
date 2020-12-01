---
UID: NF:lmserver.NetServerTransportAddEx
title: NetServerTransportAddEx function (lmserver.h)
description: The NetServerTransportAddEx function binds the specified server to the transport protocol.
helpviewer_keywords: ["0","1","2","3","NetServerTransportAddEx","NetServerTransportAddEx function [Network Management]","_win32_netservertransportaddex","lmserver/NetServerTransportAddEx","netmgmt.netservertransportaddex"]
old-location: netmgmt\netservertransportaddex.htm
tech.root: NetMgmt
ms.assetid: d1edc75d-8313-422c-a6fb-8b51a309a252
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, NetServerTransportAddEx, NetServerTransportAddEx function [Network Management], _win32_netservertransportaddex, lmserver/NetServerTransportAddEx, netmgmt.netservertransportaddex
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetServerTransportAddEx
 - lmserver/NetServerTransportAddEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetServerTransportAddEx
---

# NetServerTransportAddEx function


## -description

The 
				<b>NetServerTransportAddEx</b> function binds the specified server to the transport protocol. This extended function allows the calling application to specify the 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>, <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>, 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a>, or 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> information levels.

## -parameters

### -param servername [in]

A pointer to a string that specifies the name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param level [in]

Specifies a value that indicates the information level of the data. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the transport protocol, including name, address, and location on the network. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the transport protocol, including name, address, network location, and domain. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies the same information as level 1, with the addition of an <b>svti2_flags</b> member. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
 Specifies the same information as level 2, with the addition of credential information. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> structure.

</td>
</tr>
</table>

### -param bufptr [in]

A pointer to the buffer that contains the data. The format of this data depends on the value of the <i>level</i> parameter. 

For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUP_NAME</b></dt>
</dl>
</td>
<td width="60%">
A duplicate name exists on the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DOMAINNAME</b></dt>
</dl>
</td>
<td width="60%">
The domain name could not be found on the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid. 

This error is returned if the transport name or transport address member in the <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>, <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>, 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a>, or 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> structure pointed to by the <i>bufptr</i> parameter is <b>NULL</b>. This error is also returned if the transport address length member in the <b>SERVER_TRANSPORT_INFO_0</b>, <b>SERVER_TRANSPORT_INFO_1</b>, 
<b>SERVER_TRANSPORT_INFO_2</b>, or 
<b>SERVER_TRANSPORT_INFO_3</b> structure pointed to by the <i>bufptr</i> parameter is zero or larger than MAX_PATH (defined in the <i>Windef.h</i> header file). This error is also returned if the flags member of the <b>SERVER_TRANSPORT_INFO_2</b>, or 
<b>SERVER_TRANSPORT_INFO_3</b> structure pointed to by the <i>bufptr</i> parameter contains an illegal value.

This error is also returned for other invalid parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetServerTransportAddEx</b> function.

If you add a transport protocol to a server using a call to the 
<b>NetServerTransportAddEx</b> function, the connection will not remain after the server reboots or restarts.

The 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernameadd">NetServerComputerNameAdd</a> function is a utility function. It combines the features of the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a> function and the 
<b>NetServerTransportAddEx</b> function, allowing you to specify an emulated server name.

On Windows Server 2008  and Windows Vista with Service Pack 1 (SP1), every name registered with the Windows remote file server (SRV) is designated as either a scoped name or a non-scoped name.  Every share that is added to the system will then either be attached to all of the non-scoped names, or to a single scoped name.  Applications that wish to use the scoping features are responsible for both registering the new name as a scoped endpoint and then creating the shares with an appropriate scope. In this way, legacy uses of the Network Management and Network Share Management functions are not affected in any way since they continue to register shares and names as non-scoped names.  

A scoped endpoint is created by calling the <b>NetServerTransportAddEx</b> function with the <i>level</i> parameter set to 2 and the <i>bufptr</i> parameter pointed to a <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti2_flags</b> member. A scoped endpoint is also created by calling the <b>NetServerTransportAddEx</b> function with the <i>level</i> parameter set to 3 and the <i>bufptr</i> parameter pointed to a <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti3_flags</b> member. 

When the <b>SVTI2_SCOPED_NAME</b> bit value is set for a transport, then shares can be added with a corresponding server name (the <b>shi503_servername</b> member of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure) in a scoped fashion using the <a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a> function.  If there is no transport registered with the <b>SVTI2_SCOPED_NAME</b> bit value and the name provided in <b>shi503_servername</b> member, then the share add in a scoped fashion will not succeed.


The <a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a> function is used to add a scoped share on a remote server specified in the <i>servername</i> parameter. The remote server specified in the <b>shi503_servername</b> member of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> passed in the <i>bufptr</i> parameter must have been bound to a transport protocol using the <b>NetServerTransportAddEx</b> function as a scoped endpoint. The <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <b>shi503_servername</b> member of the <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> or <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> structure for the transport protocol.  The <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a> function is used to delete a scoped share.  The <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a> functions are to used to get and set information on a scoped share.  

Scoped endpoints are generally used by the cluster namespace.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernameadd">NetServerComputerNameAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernamedel">NetServerComputerNameDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportdel">NetServerTransportDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a>



<a href="/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>