---
UID: NS:mstcpip._SOCKET_SECURITY_SETTINGS
title: SOCKET_SECURITY_SETTINGS (mstcpip.h)
description: Specifies generic security requirements for a socket.
helpviewer_keywords: ["SOCKET_SECURITY_SETTINGS","SOCKET_SECURITY_SETTINGS structure [Winsock]","SOCKET_SETTINGS_ALLOW_INSECURE","SOCKET_SETTINGS_GUARANTEE_ENCRYPTION","mstcpip/SOCKET_SECURITY_SETTINGS","winsock.socket_security_settings"]
old-location: winsock\socket_security_settings.htm
tech.root: WinSock
ms.assetid: 9c47efb4-dd3e-4db9-a659-003292e2c5e9
ms.date: 12/05/2018
ms.keywords: SOCKET_SECURITY_SETTINGS, SOCKET_SECURITY_SETTINGS structure [Winsock], SOCKET_SETTINGS_ALLOW_INSECURE, SOCKET_SETTINGS_GUARANTEE_ENCRYPTION, mstcpip/SOCKET_SECURITY_SETTINGS, winsock.socket_security_settings
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
req.typenames: SOCKET_SECURITY_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOCKET_SECURITY_SETTINGS
 - mstcpip/_SOCKET_SECURITY_SETTINGS
 - SOCKET_SECURITY_SETTINGS
 - mstcpip/SOCKET_SECURITY_SETTINGS
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
 - SOCKET_SECURITY_SETTINGS
---

# SOCKET_SECURITY_SETTINGS structure


## -description

The <b>SOCKET_SECURITY_SETTINGS</b> structure specifies generic security requirements for  a socket.

## -struct-fields

### -field SecurityProtocol

A <a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a> value that identifies the type of security protocol to be used on the socket.

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

The <b>SOCKET_SECURITY_SETTINGS</b> structure is supported on Windows Vista and later.

The <b>SOCKET_SECURITY_SETTINGS</b> structure is used by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity">WSASetSocketSecurity</a> function to enable and apply security on  a socket.

Security settings not addressed in this structure are derived from the system default policy or the administratively configured policy. It is recommended that most applications specify a value of  <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> for the <a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a> enumeration in the <b>SecurityProtocol</b> member.  This makes the application neutral to security protocols and allows easier deployments among different systems.

Advanced applications can specify a security protocol and associated settings by casting them to the <b>SOCKET_SECURITY_SETTINGS</b> type.

## -see-also

<a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a>



<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity">WSASetSocketSecurity</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>
