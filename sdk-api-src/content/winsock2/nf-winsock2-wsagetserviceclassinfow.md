---
UID: NF:winsock2.WSAGetServiceClassInfoW
title: WSAGetServiceClassInfoW function (winsock2.h)
description: The WSAGetServiceClassInfo function retrieves the class information (schema) pertaining to a specified service class from a specified namespace provider. (Unicode)
helpviewer_keywords: ["WSAGetServiceClassInfo", "WSAGetServiceClassInfo function [Winsock]", "WSAGetServiceClassInfoW", "_win32_wsagetserviceclassinfo_2", "winsock.wsagetserviceclassinfo_2", "winsock2/WSAGetServiceClassInfo", "winsock2/WSAGetServiceClassInfoW"]
old-location: winsock\wsagetserviceclassinfo_2.htm
tech.root: WinSock
ms.assetid: e177bb7d-c7d3-43a4-a809-ab8212feea2e
ms.date: 12/05/2018
ms.keywords: WSAGetServiceClassInfo, WSAGetServiceClassInfo function [Winsock], WSAGetServiceClassInfoA, WSAGetServiceClassInfoW, _win32_wsagetserviceclassinfo_2, winsock.wsagetserviceclassinfo_2, winsock2/WSAGetServiceClassInfo, winsock2/WSAGetServiceClassInfoA, winsock2/WSAGetServiceClassInfoW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAGetServiceClassInfoW (Unicode) and WSAGetServiceClassInfoA (ANSI)
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
 - WSAGetServiceClassInfoW
 - winsock2/WSAGetServiceClassInfoW
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
 - WSAGetServiceClassInfo
 - WSAGetServiceClassInfoA
 - WSAGetServiceClassInfoW
---

# WSAGetServiceClassInfoW function


## -description

The 
<b>WSAGetServiceClassInfo</b> function retrieves the class information (schema) pertaining to a specified service class from a specified namespace provider.

## -parameters

### -param lpProviderId [in]

A pointer to a GUID that identifies a specific namespace provider.

### -param lpServiceClassId [in]

A pointer to a GUID identifying the service class.

### -param lpdwBufSize [in, out]

On input, the number of bytes contained in the buffer pointed to by the <i>lpServiceClassInfo</i> parameter. 

On output, if the function fails and the error is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a>, this parameter specifies the minimum size, in bytes, of the buffer pointed to <i>lpServiceClassInfo</i> needed to retrieve the record.

### -param lpServiceClassInfo [out]

A pointer to a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFO</a> structure that contains the service class information from the indicated namespace provider for the specified service class.

## -returns

The return value is zero if the 
<b>WSAGetServiceClassInfo</b> was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
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
The buffer pointed to by the <i>lpServiceClassInfo</i> parameter is too small to contain a WSASERVICECLASSINFOW. The application needs to pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified service class identifier or namespace provider identifier is not valid. This error is returned if the <i>lpProviderId</i>, <i>lpServiceClassId</i>, <i>lpdwBufSize</i>, or <i>lpServiceClassInfo</i> parameters are <b>NULL</b>.

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
The requested name is valid, but no data of the requested type was found.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATYPE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The specified class was not found.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAGetServiceClassInfo</b> function retrieves service class information from a namespace provider. The service class information retrieved from a particular namespace provider might not be the complete set of class information that was specified when the service class was installed. Individual namespace providers are only required to retain service class information that is applicable to the namespaces that they support. See the section 
<a href="/windows/desktop/WinSock/service-class-data-structures-in-the-spi-2">Service Class Data Structures</a> for more information.





> [!NOTE]
> The winsock2.h header defines WSAGetServiceClassInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinSock/service-class-data-structures-in-the-spi-2">Service Class Data Structures</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsainstallserviceclassa">WSAInstallServiceClass</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFOW</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
