---
UID: NS:mstcpip._SOCKET_SECURITY_SETTINGS
title: "_SOCKET_SECURITY_SETTINGS"
author: windows-sdk-content
description: Specifies generic security requirements for a socket.
old-location: winsock\socket_security_settings.htm
tech.root: WinSock
ms.assetid: 9c47efb4-dd3e-4db9-a659-003292e2c5e9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SOCKET_SECURITY_SETTINGS, SOCKET_SECURITY_SETTINGS structure [Winsock], SOCKET_SETTINGS_ALLOW_INSECURE, SOCKET_SETTINGS_GUARANTEE_ENCRYPTION, _SOCKET_SECURITY_SETTINGS, mstcpip/SOCKET_SECURITY_SETTINGS, winsock.socket_security_settings
ms.prod: windows
ms.technology: windows-sdk
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
 - SOCKET_SECURITY_SETTINGS
product: Windows
targetos: Windows
req.typenames: SOCKET_SECURITY_SETTINGS
req.redist: 
---

# _SOCKET_SECURITY_SETTINGS structure


## -description


The <b>SOCKET_SECURITY_SETTINGS</b> structure specifies generic security requirements for  a socket.


## -struct-fields




### -field SecurityProtocol

A <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> value that identifies the type of security protocol to be used on the socket.


### -field SecurityFlags

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
 


## -remarks



The <b>SOCKET_SECURITY_SETTINGS</b> structure  is supported on Windows Vistaand later.

The <b>SOCKET_SECURITY_SETTINGS</b> structure  is used by the <a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a> function to enable and apply security on  a socket.

Security settings not addressed in this structure are derived from the system default policy or the administratively configured policy. It is recommended that most applications specify a value of  <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> for the <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> enumeration in the <b>SecurityProtocol</b> member.  This makes the application neutral to security protocols and allows easier deployments among different systems.

Advanced applications can specify a security protocol and associated settings by casting them to the <b>SOCKET_SECURITY_SETTINGS</b> type.




## -see-also




<a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

