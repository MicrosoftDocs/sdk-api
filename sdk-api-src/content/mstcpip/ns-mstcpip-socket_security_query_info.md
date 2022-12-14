---
UID: NS:mstcpip._SOCKET_SECURITY_QUERY_INFO
title: SOCKET_SECURITY_QUERY_INFO (mstcpip.h)
description: Contains security information returned by the WSAQuerySocketSecurity function.
helpviewer_keywords: ["SOCKET_INFO_CONNECTION_ENCRYPTED","SOCKET_INFO_CONNECTION_SECURED","SOCKET_SECURITY_QUERY_INFO","SOCKET_SECURITY_QUERY_INFO structure [Winsock]","mstcpip/SOCKET_SECURITY_QUERY_INFO","winsock.socket_security_query_info"]
old-location: winsock\socket_security_query_info.htm
tech.root: WinSock
ms.assetid: 90439ff6-e6a8-4124-b280-a65b9ca12787
ms.date: 12/05/2018
ms.keywords: SOCKET_INFO_CONNECTION_ENCRYPTED, SOCKET_INFO_CONNECTION_SECURED, SOCKET_SECURITY_QUERY_INFO, SOCKET_SECURITY_QUERY_INFO structure [Winsock], mstcpip/SOCKET_SECURITY_QUERY_INFO, winsock.socket_security_query_info
req.header: mstcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SOCKET_SECURITY_QUERY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOCKET_SECURITY_QUERY_INFO
 - mstcpip/_SOCKET_SECURITY_QUERY_INFO
 - SOCKET_SECURITY_QUERY_INFO
 - mstcpip/SOCKET_SECURITY_QUERY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - SOCKET_SECURITY_QUERY_INFO
---

# SOCKET_SECURITY_QUERY_INFO structure


## -description

The <b>SOCKET_SECURITY_QUERY_INFO</b> structure contains security information returned by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a> function.

## -struct-fields

### -field SecurityProtocol

A <a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a> value that identifies the protocol used to secure the traffic.

### -field Flags

The  set of possible security flags for the connection defined in the <i>Mstcpip.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SOCKET_INFO_CONNECTION_SECURED"></a><a id="socket_info_connection_secured"></a><dl>
<dt><b>SOCKET_INFO_CONNECTION_SECURED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If present, traffic is being secured by a security protocol.  If absent, the traffic is flowing in the clear.

</td>
</tr>
<tr>
<td width="40%"><a id="SOCKET_INFO_CONNECTION_ENCRYPTED"></a><a id="socket_info_connection_encrypted"></a><dl>
<dt><b>SOCKET_INFO_CONNECTION_ENCRYPTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If present, the connection traffic is being encrypted.  The          <b>SOCKET_INFO_CONNECTION_SECURED</b> flag is always set when this flag is present.

</td>
</tr>
</table>

### -field PeerApplicationAccessTokenHandle

A handle to the access token that represents the account under which the peer application is running.  After using the token for access checks, the application should close the handle using the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

### -field PeerMachineAccessTokenHandle

A handle to the access token for the peer computer's account during the course of the application.  After using the token for access checks, the application should close the handle using the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

## -remarks

The <b>SOCKET_SECURITY_QUERY_INFO</b> structure  is supported on Windows Vista and later.

The <b>SOCKET_SECURITY_QUERY_INFO</b> structure  is used by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a> function to return information about the security applied to a connection on a socket.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a>



<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>