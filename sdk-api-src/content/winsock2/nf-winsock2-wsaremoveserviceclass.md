---
UID: NF:winsock2.WSARemoveServiceClass
title: WSARemoveServiceClass function (winsock2.h)
description: The WSARemoveServiceClass function permanently removes the service class schema from the registry.
helpviewer_keywords: ["WSARemoveServiceClass","WSARemoveServiceClass function [Winsock]","_win32_wsaremoveserviceclass_2","winsock.wsaremoveserviceclass_2","winsock2/WSARemoveServiceClass"]
old-location: winsock\wsaremoveserviceclass_2.htm
tech.root: WinSock
ms.assetid: 7d72f727-cca9-4a07-beb4-d64f23c1f0c1
ms.date: 12/05/2018
ms.keywords: WSARemoveServiceClass, WSARemoveServiceClass function [Winsock], _win32_wsaremoveserviceclass_2, winsock.wsaremoveserviceclass_2, winsock2/WSARemoveServiceClass
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
 - WSARemoveServiceClass
 - winsock2/WSARemoveServiceClass
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
 - WSARemoveServiceClass
---

# WSARemoveServiceClass function


## -description

The 
<b>WSARemoveServiceClass</b> function permanently removes the service class schema from the registry.

## -parameters

### -param lpServiceClassId [in]

Pointer to the GUID for the service class you want to remove.

## -returns

The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATYPE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The specified class was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to remove the Service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETOOMANYREFS</a></b></dt>
</dl>
</td>
<td width="60%">
There are service instances that still reference the class. Removal of this class is not possible at this time.

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
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified GUID was not valid.

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
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>