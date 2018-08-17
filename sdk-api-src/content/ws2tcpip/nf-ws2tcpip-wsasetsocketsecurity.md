---
UID: NF:ws2tcpip.WSASetSocketSecurity
title: WSASetSocketSecurity function
author: windows-sdk-content
description: Enables and applies security for a socket.
old-location: winsock\wsasetsocketsecurity.htm
old-project: winsock
ms.assetid: 9efee804-9763-4456-97a3-6eb9a8e30f49
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSASetSocketSecurity, WSASetSocketSecurity function [Winsock], winsock.wsasetsocketsecurity, ws2tcpip/WSASetSocketSecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ws2tcpip.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - WSASetSocketSecurity
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSASetSocketSecurity function


## -description


The <b>WSASetSocketSecurity</b> function enables and applies security for a socket.


## -parameters




### -param Socket [in]

A descriptor that identifies a socket on which security settings are being applied.


### -param SecuritySettings [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/9c47efb4-dd3e-4db9-a659-003292e2c5e9">SOCKET_SECURITY_SETTINGS</a> structure that specifies the security settings to be applied to the socket's traffic. If this parameter is <b>NULL</b>, default settings will be applied to the socket.


### -param SecuritySettingsLen [in]

The size, in bytes, of the <i>SecuritySettings</i> parameter.


### -param Overlapped [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure.  This parameter is ignored for non-overlapped sockets.


### -param CompletionRoutine [in, optional]

A pointer to the completion routine called when the operation has been completed.  This parameter is ignored for non-overlapped sockets.


## -returns



If the function succeeds, the return value is zero.  Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

Some possible error codes are listed below.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the socket passed in the <i>Socket</i> parameter was not created with an address family of the <b>AF_INET</b> or <b>AF_INET6</b> and a socket type of <b>SOCK_DGRAM</b> or <b>SOCK_STREAM</b>.  This error is also returned if the <a href="https://msdn.microsoft.com/9c47efb4-dd3e-4db9-a659-003292e2c5e9">SOCKET_SECURITY_SETTINGS</a> structure pointed to by the <i>SecuritySettings</i> parameter has an incorrect value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is connected. This function is not permitted with a connected socket, whether the socket is connection oriented or connectionless.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
A buffer passed was too small. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor passed in the <i>Socket</i> parameter is not a valid socket.

</td>
</tr>
</table>
 




## -remarks



The primary purpose of the <b>WSASetSocketSecurity</b> function is to turn on security for a socket if it is not already enabled by administrative policy. For IPsec, this means  that appropriate IPsec filters and policies will be instantiated that will be used to secure this socket. the <b>WSASetSocketSecurity</b> function can also be used to set specific security requirements for the socket.

This function simplifies having to call the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with a <i>dwIoControlCode</i> parameter set to <b>SIO_SET_SECURITY</b>.

The <b>WSASetSocketSecurity</b> function may be called on a <i>Socket</i> parameter created with an address family of <b>AF_INET</b> or <b>AF_INET6</b>.   

For a client application using connection-oriented sockets (protocol of <b>IPPROTO_TCP</b>), the <b>WSASetSocketSecurity</b> function should be called before the <a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>, <a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>, or <a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a> function is called.  If the <b>WSASetSocketSecurity</b> function is called after the <b>connect</b>, <b>ConnectEx</b>, or <b>WSAConnect</b> function,  <b>WSASetSocketSecurity</b> should fail.

For a server application using connection-oriented sockets (protocol of <b>IPPROTO_TCP</b>), the <b>WSASetSocketSecurity</b> function should be called before the <a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function is called.  If the <b>WSASetSocketSecurity</b> function is called after the <b>bind</b> function,  <b>WSASetSocketSecurity</b> should fail.

For connectionless sockets (protocol of <b>IPPROTO_UDP</b>), the application should call the <b>WSASetSocketSecurity</b> function immediately after <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> or <a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> call returns.

Server applications should call the  <a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> function to acquire exclusive access to the port used by the socket. This prevents other applications from using the same port. The <b>setsockopt</b> function would be called with the <i>level</i> parameter set to SOL_SOCKET,  the <i>optname</i> parameter set to <a href="https://msdn.microsoft.com/ce0d8188-54be-46e8-8753-d0680f690b84">SO_EXCLUSIVEADDRUSE</a>, and the <i>value </i> parameter set to nonzero. The <b>WSASetSocketSecurity</b> function internally calls the <b>setsockopt</b> with SO_EXCLUSIVEADDRUSE to obtain exclusive access to the port. This is to ensure that the socket is not vulnerable to attacks by other applications running on the local computer.

Security settings not set using the <b>WSASetSocketSecurity</b> are derived from the system default policy or the administratively configured policy. It is recommended that most applications specify a value of  <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> for the <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> enumeration in the <b>SecurityProtocol</b> member of the <b>SOCKET_SECURITY_PROTOCOL</b> pointed to by the <i>SecuritySettings</i> parameter.  This makes the application neutral to security protocols and allows easier deployments among different systems.

When the <i>SecuritySettings</i> parameter points to a <a href="https://msdn.microsoft.com/99af6ebd-6a7d-4753-8bc6-cfd42919843e">SOCKET_SECURITY_SETTINGS_IPSEC</a>  structure, the <b>SecurityProtocol</b> 
member of the structure must be set to <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b>, not <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b>.

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
<li>The application must set its security settings before calling the <a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, <a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>, <a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>, or <a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a> functions.</li>
<li>The <b>WSASetSocketSecurity</b> function can only be called once per socket.</li>
</ul>


<h3><a id="Default_Secure_Socket_IPsec_Policy"></a><a id="default_secure_socket_ipsec_policy"></a><a id="DEFAULT_SECURE_SOCKET_IPSEC_POLICY"></a>Default Secure Socket IPsec Policy</h3>
If the <i>SecuritySettings</i> parameter is set to <b>NULL</b>, and there is no other administratively specified IPsec policy on the computer, a default security policy based on IPsec will be used to secure the application's traffic.  Some type of authentication credential (a user certificate or domain membership, for example) must be present for IPsec to succeed with a default policy.


The default IPsec policy has been designed so that IPsec security can be negotiated in as many scenarios as possible.

<pre class="syntax" xml:space="preserve"><code>Authip MM policy = 
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
</code></pre>



## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=86174">AuthIP in Windows Vista</a>



<a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a>



<a href="https://msdn.microsoft.com/9c47efb4-dd3e-4db9-a659-003292e2c5e9">SOCKET_SECURITY_SETTINGS</a>



<a href="https://msdn.microsoft.com/99af6ebd-6a7d-4753-8bc6-cfd42919843e">SOCKET_SECURITY_SETTINGS_IPSEC</a>



<a href="https://msdn.microsoft.com/ce0d8188-54be-46e8-8753-d0680f690b84">SO_EXCLUSIVEADDRUSE</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/5d973316-fc51-453e-8d98-36ba36367df7">WSADeleteSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/8dd2c0dd-ca1d-40b8-8e58-a980e67b6941">WSAImpersonateSocketPeer</a>



<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/7de25015-97ec-4338-846f-57df54142d65">WSARevertImpersonation</a>



<a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

