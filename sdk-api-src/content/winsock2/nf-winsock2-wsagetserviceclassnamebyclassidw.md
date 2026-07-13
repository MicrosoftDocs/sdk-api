---
UID: NF:winsock2.WSAGetServiceClassNameByClassIdW
title: WSAGetServiceClassNameByClassIdW function (winsock2.h)
description: The WSAGetServiceClassNameByClassId function retrieves the name of the service associated with the specified type. This name is the generic service name, like FTP or SNA, and not the name of a specific instance of that service. (Unicode)
helpviewer_keywords: ["WSAGetServiceClassNameByClassId", "WSAGetServiceClassNameByClassId function [Winsock]", "WSAGetServiceClassNameByClassIdW", "_win32_wsagetserviceclassnamebyclassid_2", "winsock.wsagetserviceclassnamebyclassid_2", "winsock2/WSAGetServiceClassNameByClassId", "winsock2/WSAGetServiceClassNameByClassIdW"]
old-location: winsock\wsagetserviceclassnamebyclassid_2.htm
tech.root: WinSock
ms.assetid: 0a61751e-10e5-4f91-a0b2-8c1baf477653
ms.date: 12/05/2018
ms.keywords: WSAGetServiceClassNameByClassId, WSAGetServiceClassNameByClassId function [Winsock], WSAGetServiceClassNameByClassIdA, WSAGetServiceClassNameByClassIdW, _win32_wsagetserviceclassnamebyclassid_2, winsock.wsagetserviceclassnamebyclassid_2, winsock2/WSAGetServiceClassNameByClassId, winsock2/WSAGetServiceClassNameByClassIdA, winsock2/WSAGetServiceClassNameByClassIdW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAGetServiceClassNameByClassIdW (Unicode) and WSAGetServiceClassNameByClassIdA (ANSI)
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
 - WSAGetServiceClassNameByClassIdW
 - winsock2/WSAGetServiceClassNameByClassIdW
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
 - WSAGetServiceClassNameByClassId
 - WSAGetServiceClassNameByClassIdA
 - WSAGetServiceClassNameByClassIdW
---

# WSAGetServiceClassNameByClassIdW function


## -description

The 
<b>WSAGetServiceClassNameByClassId</b> function retrieves the name of the service associated with the specified type. This name is the generic service name, like FTP or SNA, and not the name of a specific instance of that service.

## -parameters

### -param lpServiceClassId [in]

A pointer to the GUID for the service class.

### -param lpszServiceClassName [out]

A pointer to the service name.

### -param lpdwBufferLength [in, out]

On input, the length of the buffer returned by <i>lpszServiceClassName</i>, in characters. On output, the length of the service name copied into <i>lpszServiceClassName</i>, in characters.

## -returns

The 
<b>WSAGetServiceClassNameByClassId</b> function returns a value of zero if successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_PARAMETER</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpServiceClassId</i> parameter specified is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to access the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified buffer pointed to by <i>lpszServiceClassName</i> is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported for the type of object referenced. This error is returned by some namespace providers that do not support getting service class information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpServiceClassId</i> is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

## -remarks

> [!NOTE]
> The winsock2.h header defines WSAGetServiceClassNameByClassId as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
