---
UID: NF:winsock2.WSAGetQOSByName
title: WSAGetQOSByName function (winsock2.h)
description: The WSAGetQOSByName function initializes a QOS structure based on a named template, or it supplies a buffer to retrieve an enumeration of the available template names.
helpviewer_keywords: ["WSAGetQOSByName","WSAGetQOSByName function [Winsock]","_win32_wsagetqosbyname_2","winsock.wsagetqosbyname_2","winsock2/WSAGetQOSByName"]
old-location: winsock\wsagetqosbyname_2.htm
tech.root: WinSock
ms.assetid: 9b586856-5441-414b-8b91-298c952c351b
ms.date: 12/05/2018
ms.keywords: WSAGetQOSByName, WSAGetQOSByName function [Winsock], _win32_wsagetqosbyname_2, winsock.wsagetqosbyname_2, winsock2/WSAGetQOSByName
req.header: winsock2.h
req.include-header: 
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSAGetQOSByName
 - winsock2/WSAGetQOSByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAGetQOSByName
---

# WSAGetQOSByName function


## -description

The 
<b>WSAGetQOSByName</b> function initializes a 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure based on a named template, or it supplies a buffer to retrieve an enumeration of the available template names.

## -parameters

### -param s [in]

A descriptor identifying a socket.

### -param lpQOSName [in, out]

A pointer to a specific quality of service template.

### -param lpQOS [out]

A pointer to the 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure to be filled.

## -returns

If 
<b>WSAGetQOSByName</b> succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpQOSName</i> or <i>lpQOS</i> parameter are not a valid part of the user address space, or the buffer length for <i>lpQOS</i> is too small.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAGetQOSByName</b> function is used by applications to initialize a 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure to a set of known values appropriate for a particular service class or media type. These values are stored in a template that is referenced by a well-known name. The client may retrieve these values by setting the <i>buf</i> parameter of the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structure indicated by <i>lpQOSName</i>, which points to a string of nonzero length specifying a template name. In this case, the usage of <i>lpQOSName</i> is IN only, and results are returned through <i>lpQOS</i>.

Alternatively, the client may use this function to retrieve an enumeration of available template names. The client may do this by setting the <i>buf</i> parameter of the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> indicated by <i>lpQOSName</i> to a zero-length null-terminated string. In this case the buffer indicated by <i>buf</i> is overwritten with a sequence of as many available, null-terminated template names up to the number of bytes available in <i>buf</i> as indicated by the <i>len</i> parameter of the 
<b>WSABUF</b> indicated by <i>lpQOSName</i>. The list of names itself is terminated by a zero-length name. When the 
<b>WSAGetQOSByName</b> function is used to retrieve template names, the <i>lpQOS</i> parameter is ignored.

## -see-also

<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>