---
UID: NF:winsock2.WSAInstallServiceClassW
title: WSAInstallServiceClassW function (winsock2.h)
description: The WSAInstallServiceClass function registers a service class schema within a namespace. (Unicode)
helpviewer_keywords: ["WSAInstallServiceClass", "WSAInstallServiceClass function [Winsock]", "WSAInstallServiceClassW", "_win32_wsainstallserviceclass_2", "winsock.wsainstallserviceclass_2", "winsock2/WSAInstallServiceClass", "winsock2/WSAInstallServiceClassW"]
old-location: winsock\wsainstallserviceclass_2.htm
tech.root: WinSock
ms.assetid: 06760319-aeeb-4ad7-b77a-01efea7ed904
ms.date: 12/05/2018
ms.keywords: WSAInstallServiceClass, WSAInstallServiceClass function [Winsock], WSAInstallServiceClassA, WSAInstallServiceClassW, _win32_wsainstallserviceclass_2, winsock.wsainstallserviceclass_2, winsock2/WSAInstallServiceClass, winsock2/WSAInstallServiceClassA, winsock2/WSAInstallServiceClassW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAInstallServiceClassW (Unicode) and WSAInstallServiceClassA (ANSI)
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
 - WSAInstallServiceClassW
 - winsock2/WSAInstallServiceClassW
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
 - WSAInstallServiceClass
 - WSAInstallServiceClassA
 - WSAInstallServiceClassW
---

# WSAInstallServiceClassW function


## -description

The 
<b>WSAInstallServiceClass</b> function registers a service class schema within a namespace. This schema includes the class name, class identifier, and any namespace-specific information that is common to all instances of the service, such as the SAP identifier or object identifier.

## -parameters

### -param lpServiceClassInfo [in]

Service class to namespace specific–type mapping information. Multiple mappings can be handled at one time. 




See the section 
<a href="/windows/desktop/WinSock/name-resolution-data-structures-2">Service Class Data Structures</a> for a description of pertinent data structures.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_PARAMETER</a></b></dt>
</dl>
</td>
<td width="60%">
The namespace provider cannot supply the requested class information.

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
The calling function does not have sufficient privileges to install the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
Service class information has already been registered for this service class identifier. To modify service class information, first use 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaremoveserviceclass">WSARemoveServiceClass</a>, and then reinstall with updated class information data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The service class information was not valid or improperly structured. This error is returned if the <i>lpServiceClassInfo</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

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
</table>

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetserviceclassinfoa">WSAGetServiceClassInfo</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFO</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

## -remarks

> [!NOTE]
> The winsock2.h header defines WSAInstallServiceClass as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
