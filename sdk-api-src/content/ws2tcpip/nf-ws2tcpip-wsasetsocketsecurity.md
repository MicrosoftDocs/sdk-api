---
UID: NF:ws2tcpip.WSASetSocketSecurity
title: WSASetSocketSecurity function (ws2tcpip.h)
description: Enables and applies security for a socket.
helpviewer_keywords: ["WSASetSocketSecurity","WSASetSocketSecurity function [Winsock]","winsock.wsasetsocketsecurity","ws2tcpip/WSASetSocketSecurity"]
old-location: winsock\wsasetsocketsecurity.htm
tech.root: WinSock
ms.assetid: 9efee804-9763-4456-97a3-6eb9a8e30f49
ms.date: 12/05/2018
ms.keywords: WSASetSocketSecurity, WSASetSocketSecurity function [Winsock], winsock.wsasetsocketsecurity, ws2tcpip/WSASetSocketSecurity
req.header: ws2tcpip.h
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSASetSocketSecurity
 - ws2tcpip/WSASetSocketSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - WSASetSocketSecurity
---

# WSASetSocketSecurity function


## -description

The <b>WSASetSocketSecurity</b> function enables and applies security for a socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a socket on which security settings are being applied.

### -param SecuritySettings [in, optional]

A pointer to a <a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_security_settings">SOCKET_SECURITY_SETTINGS</a> structure that specifies the security settings to be applied to the socket's traffic. If this parameter is <b>NULL</b>, default settings will be applied to the socket.

### -param SecuritySettingsLen [in]

The size, in bytes, of the <i>SecuritySettings</i> parameter.

### -param Overlapped [in, optional]

A pointer to a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.  This parameter is ignored for non-overlapped sockets.

### -param CompletionRoutine [in, optional]

A pointer to the completion routine called when the operation has been completed.  This parameter is ignored for non-overlapped sockets.

## -returns

If the function succeeds, the return value is zero.  Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

Some possible error codes are listed below.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the socket passed in the <i>Socket</i> parameter was not created with an address family of the <b>AF_INET</b> or <b>AF_INET6</b> and a socket type of <b>SOCK_DGRAM</b> or <b>SOCK_STREAM</b>.  This error is also returned if the <a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_security_settings">SOCKET_SECURITY_SETTINGS</a> structure pointed to by the <i>SecuritySettings</i> parameter has an incorrect value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is connected. This function is not permitted with a connected socket, whether the socket is connection oriented or connectionless.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
A buffer passed was too small. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor passed in the <i>Socket</i> parameter is not a valid socket.

</td>
</tr>
</table>

## -remarks

The primary purpose of the <b>WSASetSocketSecurity</b> function is to turn on security for a socket if it is not already enabled by administrative policy. For IPsec, this means  that appropriate IPsec filters and policies will be instantiated that will be used to secure this socket. the <b>WSASetSocketSecurity</b> function can also be used to set specific security requirements for the socket.

This function simplifies having to call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with a <i>dwIoControlCode</i> parameter set to <b>SIO_SET_SECURITY</b>.

The <b>WSASetSocketSecurity</b> function may be called on a <i>Socket</i> parameter created with an address family of <b>AF_INET</b> or <b>AF_INET6</b>.   

For a client application using connection-oriented sockets (protocol of <b>IPPROTO_TCP</b>), the <b>WSASetSocketSecurity</b> function should be called before the <a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>, <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>, or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> function is called.  If the <b>WSASetSocketSecurity</b> function is called after the <b>connect</b>, <b>ConnectEx</b>, or <b>WSAConnect</b> function,  <b>WSASetSocketSecurity</b> should fail.

For a server application using connection-oriented sockets (protocol of <b>IPPROTO_TCP</b>), the <b>WSASetSocketSecurity</b> function should be called before the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function is called.  If the <b>WSASetSocketSecurity</b> function is called after the <b>bind</b> function,  <b>WSASetSocketSecurity</b> should fail.

For connectionless sockets (protocol of <b>IPPROTO_UDP</b>), the application should call the <b>WSASetSocketSecurity</b> function immediately after <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> call returns.

Server applications should call the  <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function to acquire exclusive access to the port used by the socket. This prevents other applications from using the same port. The <b>setsockopt</b> function would be called with the <i>level</i> parameter set to SOL_SOCKET,  the <i>optname</i> parameter set to <a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a>, and the <i>value </i> parameter set to nonzero. The <b>WSASetSocketSecurity</b> function internally calls the <b>setsockopt</b> with SO_EXCLUSIVEADDRUSE to obtain exclusive access to the port. This is to ensure that the socket is not vulnerable to attacks by other applications running on the local computer.

Security settings not set using the <b>WSASetSocketSecurity</b> are derived from the system default policy or the administratively configured policy. It is recommended that most applications specify a value of  <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> for the <a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a> enumeration in the <b>SecurityProtocol</b> member of the <b>SOCKET_SECURITY_PROTOCOL</b> pointed to by the <i>SecuritySettings</i> parameter.  This makes the application neutral to security protocols and allows easier deployments among different systems.

When the <i>SecuritySettings</i> parameter points to a <a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_security_settings_ipsec">SOCKET_SECURITY_SETTINGS_IPSEC</a>  structure, the <b>SecurityProtocol</b> 
member of the structure must be set to <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b>, not <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b>.

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
<li>The application must set its security settings before calling the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>, <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>, or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> functions.</li>
<li>The <b>WSASetSocketSecurity</b> function can only be called once per socket.</li>
</ul>


<h3><a id="Default_Secure_Socket_IPsec_Policy"></a><a id="default_secure_socket_ipsec_policy"></a><a id="DEFAULT_SECURE_SOCKET_IPSEC_POLICY"></a>Default Secure Socket IPsec Policy</h3>
If the <i>SecuritySettings</i> parameter is set to <b>NULL</b>, and there is no other administratively specified IPsec policy on the computer, a default security policy based on IPsec will be used to secure the application's traffic.  Some type of authentication credential (a user certificate or domain membership, for example) must be present for IPsec to succeed with a default policy.


The default IPsec policy has been designed so that IPsec security can be negotiated in as many scenarios as possible.


``` syntax
Authip MM policy = 
{
 Auth methods = {IKE_ANONYMOUS}
 No impersonation
 Proposals = 
 {
   {
     Crypto algos = 
     IKE_CIPHER_AES_128,
     IKE_INTEGRITY_SHA1, 
     IKE_DH_ECP_256
     MM lifetime = 2 hrs
     QM = 0 (infinite)
   }
   {
     Crypto algos = 
     IKE_CIPHER_3DES, 
     IKE_INTEGRITY_SHA1, 
     IKE_DH_GROUP_2
     MM lifetime = 2 hrs
     QM = 0 (infinite)
   }
 }
}

Authip QM policy =
{
 QM proposals = 
 {
   QM lifetime = 1 hr, 55GB,
   Crypto algos = 
   IPSEC_TRANSFORM_ESP_AUTH, 
   IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_1_96
   No PFS
 }
 {
   QM lifetime = 1 hr, 55GB,
   Crypto algos = 
   IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER,
   IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_1_96,
   IPSEC_CIPHER_TRANSFORM_ID_AES_128
   No PFS
 }
 {
   QM lifetime = 1 hr, 55GB,
   Crypto algos = 
   IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER,
   IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_1_96,
   IPSEC_CIPHER_TRANSFORM_ID_CBC_3DES
   No PFS
 }
 {
   QM lifetime = 1 hr, 55GB,
   Crypto algos = 
   IPSEC_TRANSFORM_AH,
   IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_1_96
   No PFS
 }
 IPSEC_POLICY_FLAG_ND_BOUNDARY
 ndAllowClearTimeoutSeconds = 10
 saIdleTimeout = {5mins, 1min}
 UM policy = 
 {
   {IKE_SSL, Null-Root-Config}
   {IKE_KERBEROS}
   {IKE_SSL, Null-Root-Config}
   No impersonation
 } 
}

```


## -see-also

<a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_security_settings">SOCKET_SECURITY_SETTINGS</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_security_settings_ipsec">SOCKET_SECURITY_SETTINGS_IPSEC</a>



<a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a>



<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname">WSADeleteSocketPeerTargetName</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer">WSAImpersonateSocketPeer</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsarevertimpersonation">WSARevertImpersonation</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname">WSASetSocketPeerTargetName</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity">WSASetSocketSecurity</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>
