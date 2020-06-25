---
UID: NF:ws2tcpip.WSARevertImpersonation
title: WSARevertImpersonation function (ws2tcpip.h)
description: Terminates the impersonation of a socket peer. This must be called after calling WSAImpersonateSocketPeer and finishing any access checks.
helpviewer_keywords: ["WSARevertImpersonation","WSARevertImpersonation function [Winsock]","winsock.wsarevertimpersonation","ws2tcpip/WSARevertImpersonation"]
old-location: winsock\wsarevertimpersonation.htm
tech.root: WinSock
ms.assetid: 7de25015-97ec-4338-846f-57df54142d65
ms.date: 12/05/2018
ms.keywords: WSARevertImpersonation, WSARevertImpersonation function [Winsock], winsock.wsarevertimpersonation, ws2tcpip/WSARevertImpersonation
f1_keywords:
- ws2tcpip/WSARevertImpersonation
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Fwpuclnt.dll
api_name:
- WSARevertImpersonation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSARevertImpersonation function


## -description


The <b>WSARevertImpersonation</b> function terminates the impersonation of a socket peer.  This must be called after calling <a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer">WSAImpersonateSocketPeer</a> and finishing any access checks.


## -parameters






## -returns



If the function succeeds, the return value is zero.  Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>. 

Some possible error codes are listed below.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASYSCALLFAILURE</a></b></dt>
</dl>
</td>
<td width="60%">
 A system call that should never fail has failed.

</td>
</tr>
</table>
 




## -remarks



The <b>WSARevertImpersonation</b> function causes the calling thread to discontinue
    the impersonation of a socket peer. If the thread is not currently
    impersonating a socket peer, no action is taken.

The <b>WSARevertImpersonation</b> function should be called after calling <a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer">WSAImpersonateSocketPeer</a> and all access checks are finished.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname">WSADeleteSocketPeerTargetName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer">WSAImpersonateSocketPeer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname">WSASetSocketPeerTargetName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity">WSASetSocketSecurity</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>
 

 

