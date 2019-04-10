---
UID: NS:mstcpip._SOCKET_SECURITY_SETTINGS_IPSEC
title: SOCKET_SECURITY_SETTINGS_IPSEC (mstcpip.h)
author: windows-sdk-content
description: Specifies various security requirements and settings that are specific to IPsec.
old-location: winsock\socket_security_settings_ipsec.htm
tech.root: WinSock
ms.assetid: 99af6ebd-6a7d-4753-8bc6-cfd42919843e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SOCKET_SECURITY_SETTINGS_IPSEC, SOCKET_SECURITY_SETTINGS_IPSEC structure [Winsock], SOCKET_SETTINGS_ALLOW_INSECURE, SOCKET_SETTINGS_GUARANTEE_ENCRYPTION, SOCKET_SETTINGS_IPSEC_SKIP_FILTER_INSTANTIATION, mstcpip/SOCKET_SECURITY_SETTINGS_IPSEC, winsock.socket_security_settings_ipsec
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - SOCKET_SECURITY_SETTINGS_IPSEC
product: Windows
targetos: Windows
req.typenames: SOCKET_SECURITY_SETTINGS_IPSEC
req.redist: 
---

# SOCKET_SECURITY_SETTINGS_IPSEC structure


## -description


The <b>SOCKET_SECURITY_SETTINGS_IPSEC</b> structure specifies various security requirements and settings that are specific to IPsec.


## -struct-fields




### -field SecurityProtocol

Type: <b>SOCKET_SECURITY_PROTOCOL</b>

A <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> value that identifies the type of security protocol to be used on the socket. This member must be set to <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b>.


### -field SecurityFlags

Type: <b>ULONG</b>

A set of flags that allow applications to set specific security requirements on a socket. The possible values are defined in the <i>Mstcpip.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SOCKET_SETTINGS_GUARANTEE_ENCRYPTION"></a><a id="socket_settings_guarantee_encryption"></a><dl>
<dt><b>SOCKET_SETTINGS_GUARANTEE_ENCRYPTION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates that guaranteed encryption of traffic is required.  This flag should be set if the default policy prefers methods of protection that do not use encryption. If this flag is set and encryption is not possible for any reason, no packets will be sent and a connection will not be established.

</td>
</tr>
<tr>
<td width="40%"><a id="SOCKET_SETTINGS_ALLOW_INSECURE"></a><a id="socket_settings_allow_insecure"></a><dl>
<dt><b>SOCKET_SETTINGS_ALLOW_INSECURE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Indicates that clear text connections are allowed.  If this flag is set, some or all of the sent packets will be sent in clear text, especially if security with the peer could not be negotiated.

<div class="alert"><b>Note</b>  If this flag is not set, it is guaranteed that packets will never be sent in clear text, even if security negotiation fails.</div>
<div> </div>
</td>
</tr>
</table>
 


### -field IpsecFlags

Type: <b>ULONG</b>

Flags for IPsec security settings. The possible values are defined in the <i>Mstcpip.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SOCKET_SETTINGS_IPSEC_SKIP_FILTER_INSTANTIATION"></a><a id="socket_settings_ipsec_skip_filter_instantiation"></a><dl>
<dt><b>SOCKET_SETTINGS_IPSEC_SKIP_FILTER_INSTANTIATION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
When this flag is set, IPsec filter instantiation is omitted for the socket.  This flag should be set when an application knows that IPsec filters and policy already exist for its traffic.  Applications running on a domain with IPsec policy in place can also set this flag.

</td>
</tr>
</table>
 


### -field AuthipMMPolicyKey

Type: <b>GUID</b>

The GUID for the Windows Filtering Platform key of the AuthIP main mode provider context.  If an application wishes to use a custom main mode policy, it should first use the <a href="https://msdn.microsoft.com/c31595b8-81e4-4399-b2a3-d228c35875fe">FwpmProviderContextAdd0</a> function to add the corresponding provider context and specify the returned key in this member.  This field is ignored for a GUID of zero. 


### -field AuthipQMPolicyKey

Type: <b>GUID</b>

The Windows Filtering Platform key of the AuthIp quick mode provider context.  If an application wishes to use a custom quick mode policy, it should first use the <a href="https://msdn.microsoft.com/c31595b8-81e4-4399-b2a3-d228c35875fe">FwpmProviderContextAdd0</a> function to add the corresponding provider context and specify the returned key in this field.  This field is ignored for a GUID of zero. 


### -field Reserved

Type: <b>GUID</b>

Reserved for future use.


### -field Reserved2

Type: <b>UINT64</b>

Reserved for future use.


### -field UserNameStringLen

Type: <b>ULONG</b>

The length, in bytes, of the user name in the <b>AllStrings</b> member.


### -field DomainNameStringLen

Type: <b>ULONG</b>

The length, in bytes, of the domain name in the <b>AllStrings</b> member.


### -field PasswordStringLen

Type: <b>ULONG</b>

The length, in bytes, of the password in the <b>AllStrings</b> member.


### -field AllStrings

Type: <b>wchar_t[]</b>

A string that contains the user name, the domain name, and the password concatenated in this order.


## -remarks



The <b>SOCKET_SECURITY_SETTINGS_IPSEC</b> structure  is supported on Windows Vistaand later.

The <b>SOCKET_SECURITY_SETTINGS_IPSEC</b> structure  is meant to be used by an advanced application that requires more flexibility and wishes to customize IPSec policy for their traffic. The pointer to the <b>SOCKET_SECURITY_SETTINGS_IPSEC</b> structure needs to cast to the <a href="https://msdn.microsoft.com/9c47efb4-dd3e-4db9-a659-003292e2c5e9">SOCKET_SECURITY_SETTINGS</a> structure  type when calling the <a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a> function to enable and apply security on  a socket. 

The <b>SecurityProtocol</b> 
member of the <b>SOCKET_SECURITY_SETTINGS_IPSEC</b>  structure must be set to <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b>, not <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b>.

To simplify Internet Protocol security (IPsec) deployment, Windows Vista and later support an enhanced version of the Internet Key Exchange (IKE) protocol known as Authenticated Internet Protocol (AuthIP). AuthIP provides simplified IPsec policy configuration and maintenance in many configurations and additional flexibility for IPsec peer authentication.

There is a possibility that some of the IPsec settings specified in the <b>SOCKET_SECURITY_SETTINGS_IPSEC</b> structure may end up being different from the actual settings applied to the network traffic on a socket. For example, this could happen when an application specifies custom main mode or quick mode policy, but a different policy with a higher priority (a domain policy, for example) specifies conflicting settings for the same traffic. To be aware of such conflicts, an application can use the Windows Filtering Platform API to query the policy being applied and subscribe for notifications.




## -see-also




<a href="https://msdn.microsoft.com/6faad008-b2f6-4f45-89c7-ae98c2f58ce1">About Windows Filtering Platform</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=86174">AuthIP in Windows Vista</a>



<a href="https://msdn.microsoft.com/c31595b8-81e4-4399-b2a3-d228c35875fe">FwpmProviderContextAdd0</a>



<a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a>



<a href="https://msdn.microsoft.com/9c47efb4-dd3e-4db9-a659-003292e2c5e9">SOCKET_SECURITY_SETTINGS</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

