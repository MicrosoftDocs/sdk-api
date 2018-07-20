---
UID: NF:ws2tcpip.WSARevertImpersonation
title: WSARevertImpersonation function
author: windows-sdk-content
description: Terminates the impersonation of a socket peer. This must be called after calling WSAImpersonateSocketPeer and finishing any access checks.
old-location: winsock\wsarevertimpersonation.htm
old-project: winsock
ms.assetid: 7de25015-97ec-4338-846f-57df54142d65
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: WSARevertImpersonation, WSARevertImpersonation function [Winsock], winsock.wsarevertimpersonation, ws2tcpip/WSARevertImpersonation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - WSARevertImpersonation
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSARevertImpersonation function


## -description


The <b>WSARevertImpersonation</b> function terminates the impersonation of a socket peer.  This must be called after calling <a href="https://msdn.microsoft.com/8dd2c0dd-ca1d-40b8-8e58-a980e67b6941">WSAImpersonateSocketPeer</a> and finishing any access checks.


## -parameters






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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSASYSCALLFAILURE</a></b></dt>
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

The <b>WSARevertImpersonation</b> function should be called after calling <a href="https://msdn.microsoft.com/8dd2c0dd-ca1d-40b8-8e58-a980e67b6941">WSAImpersonateSocketPeer</a> and all access checks are finished.




## -see-also




<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/5d973316-fc51-453e-8d98-36ba36367df7">WSADeleteSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/8dd2c0dd-ca1d-40b8-8e58-a980e67b6941">WSAImpersonateSocketPeer</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

