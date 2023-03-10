---
UID: NS:lmserver._SERVER_TRANSPORT_INFO_1
title: SERVER_TRANSPORT_INFO_1 (lmserver.h)
description: The SERVER_TRANSPORT_INFO_1 structure contains information about the specified transport protocol, including name and address. This information level is valid only for the NetServerTransportAddEx function.
helpviewer_keywords: ["*LPSERVER_TRANSPORT_INFO_1","*PSERVER_TRANSPORT_INFO_1","LPSERVER_TRANSPORT_INFO_1","LPSERVER_TRANSPORT_INFO_1 structure pointer [Network Management]","PSERVER_TRANSPORT_INFO_1","PSERVER_TRANSPORT_INFO_1 structure pointer [Network Management]","SERVER_TRANSPORT_INFO_1","SERVER_TRANSPORT_INFO_1 structure [Network Management]","_win32_server_transport_info_1_str","lmserver/LPSERVER_TRANSPORT_INFO_1","lmserver/PSERVER_TRANSPORT_INFO_1","lmserver/SERVER_TRANSPORT_INFO_1","netmgmt.server_transport_info_1_str"]
old-location: netmgmt\server_transport_info_1_str.htm
tech.root: NetMgmt
ms.assetid: f21fed49-207a-4f64-becd-3d3c1e995eb0
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_TRANSPORT_INFO_1, *PSERVER_TRANSPORT_INFO_1, LPSERVER_TRANSPORT_INFO_1, LPSERVER_TRANSPORT_INFO_1 structure pointer [Network Management], PSERVER_TRANSPORT_INFO_1, PSERVER_TRANSPORT_INFO_1 structure pointer [Network Management], SERVER_TRANSPORT_INFO_1, SERVER_TRANSPORT_INFO_1 structure [Network Management], _win32_server_transport_info_1_str, lmserver/LPSERVER_TRANSPORT_INFO_1, lmserver/PSERVER_TRANSPORT_INFO_1, lmserver/SERVER_TRANSPORT_INFO_1, netmgmt.server_transport_info_1_str'
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
req.typenames: SERVER_TRANSPORT_INFO_1, *PSERVER_TRANSPORT_INFO_1, *LPSERVER_TRANSPORT_INFO_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_TRANSPORT_INFO_1
 - lmserver/_SERVER_TRANSPORT_INFO_1
 - PSERVER_TRANSPORT_INFO_1
 - lmserver/PSERVER_TRANSPORT_INFO_1
 - SERVER_TRANSPORT_INFO_1
 - lmserver/SERVER_TRANSPORT_INFO_1
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
 - SERVER_TRANSPORT_INFO_1
---

# SERVER_TRANSPORT_INFO_1 structure


## -description

The 
				<b>SERVER_TRANSPORT_INFO_1</b> structure contains information about the specified transport protocol, including name and address. This information level is valid only for the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.

## -struct-fields

### -field svti1_numberofvcs

Type: <b>DWORD</b>

The number of clients connected to the server that are using the transport protocol specified by the <b>svti1_transportname</b> member.

### -field svti1_transportname

Type: <b>LMSTR</b>

A pointer to a null-terminated character string that contains the name of a transport device; for example,


``` syntax
\Device\NetBT_Tcpip_{2C9725F4-151A-11D3-AEEC-C3B211BD350B}

```

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field svti1_transportaddress

Type: <b>LPBYTE</b>

A pointer to a variable that contains the address the server is using on the transport device specified by the <b>svti1_transportname</b> member.

This member is usually the NetBIOS name that the server is using. In these instances, the name must be 16 characters long, and the last character must be a blank character (0x20).

### -field svti1_transportaddress.size_is

### -field svti1_transportaddress.size_is.svti1_transportaddresslength

### -field svti1_transportaddresslength

Type: <b>DWORD</b>

The length, in bytes, of the <b>svti1_transportaddress</b> member. For NetBIOS names, the value of this member is 16 (decimal).

### -field svti1_networkaddress

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the address the network adapter is using. The string is transport-specific.

You can retrieve this value only with a call to the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a> function. You cannot set this value with a call to the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a> function or the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field svti1_domain

Type: <b>LMSTR</b>

A pointer to a NULL-terminated character string that contains the name of the domain to which the server should announce its presence. (When you call 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>, this member is the name of the domain to which the server is announcing its presence.)

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

## -remarks

The 
				<b>SERVER_TRANSPORT_INFO_1</b> structure is used by the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function to bind the specified server to the transport protocol.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernameadd">NetServerComputerNameAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernamedel">NetServerComputerNameDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportdel">NetServerTransportDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a>



<a href="/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>
