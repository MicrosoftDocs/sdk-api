---
UID: NS:mstcpip._SOCKET_PEER_TARGET_NAME
title: SOCKET_PEER_TARGET_NAME (mstcpip.h)
description: Contains the IP address and name for a peer target and the type of security protocol to be used on a socket.
helpviewer_keywords: ["SOCKET_PEER_TARGET_NAME","SOCKET_PEER_TARGET_NAME structure [Winsock]","mstcpip/SOCKET_PEER_TARGET_NAME","winsock.socket_peer_target_name"]
old-location: winsock\socket_peer_target_name.htm
tech.root: WinSock
ms.assetid: 6e807cc3-f9de-4d15-b337-4a6b4be910c2
ms.date: 12/05/2018
ms.keywords: SOCKET_PEER_TARGET_NAME, SOCKET_PEER_TARGET_NAME structure [Winsock], mstcpip/SOCKET_PEER_TARGET_NAME, winsock.socket_peer_target_name
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
req.typenames: SOCKET_PEER_TARGET_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOCKET_PEER_TARGET_NAME
 - mstcpip/_SOCKET_PEER_TARGET_NAME
 - SOCKET_PEER_TARGET_NAME
 - mstcpip/SOCKET_PEER_TARGET_NAME
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
 - SOCKET_PEER_TARGET_NAME
---

# SOCKET_PEER_TARGET_NAME structure


## -description

The <b>SOCKET_PEER_TARGET_NAME</b> structure contains the IP address and name for a peer target and the type of security protocol to be used on a socket.

## -struct-fields

### -field SecurityProtocol

A <a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a> value that identifies the type of protocol used to secure the traffic on the socket.

### -field PeerAddress

The IP address of the peer for the socket.

### -field PeerTargetNameStringLen

The length, in bytes, of the peer target name in the <b>AllStrings</b> member.

### -field AllStrings

The peer target name for the socket.

## -remarks

The <b>SOCKET_PEER_TARGET_NAME</b> structure  is supported on Windows Vista and later.

The <b>SOCKET_PEER_TARGET_NAME</b> structure  is used by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname">WSASetSocketPeerTargetName</a> function to specify the peer target name that corresponds to a peer IP address.  This target name is meant to be specified by client applications to securely identify the peer that should be authenticated.

Currently, the only type of security protocol that is supported is IPsec. So specifying an enumeration value  of <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> has the same effect as specifying <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b> in the <b>SecurityProtocol</b> member. 

The implementation of IPsec on Windows Vista and Windows Server 2008 only supports computer-to-computer and user-to-computer authentication. As a result, the peer target name specified in the <b>AllStrings</b> member of the <b>SOCKET_PEER_TARGET_NAME</b> structure  should refer to the peer computer principal.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a>



<a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a>



<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname">WSASetSocketPeerTargetName</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>
