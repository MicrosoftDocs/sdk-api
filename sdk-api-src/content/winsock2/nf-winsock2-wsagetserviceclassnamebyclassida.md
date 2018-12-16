---
UID: NF:winsock2.WSAGetServiceClassNameByClassIdA
title: WSAGetServiceClassNameByClassIdA function
author: windows-sdk-content
description: The WSAGetServiceClassNameByClassId function retrieves the name of the service associated with the specified type. This name is the generic service name, like FTP or SNA, and not the name of a specific instance of that service.
old-location: winsock\wsagetserviceclassnamebyclassid_2.htm
tech.root: winsock
ms.assetid: 0a61751e-10e5-4f91-a0b2-8c1baf477653
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSAGetServiceClassNameByClassId, WSAGetServiceClassNameByClassId function [Winsock], WSAGetServiceClassNameByClassIdA, WSAGetServiceClassNameByClassIdW, _win32_wsagetserviceclassnamebyclassid_2, winsock.wsagetserviceclassnamebyclassid_2, winsock2/WSAGetServiceClassNameByClassId, winsock2/WSAGetServiceClassNameByClassIdA, winsock2/WSAGetServiceClassNameByClassIdW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSAGetServiceClassNameByClassIdA function


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
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_INVALID_PARAMETER</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpServiceClassId</i> parameter specified is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to access the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified buffer pointed to by <i>lpszServiceClassName</i> is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported for the type of object referenced. This error is returned by some namespace providers that do not support getting service class information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpServiceClassId</i> is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

