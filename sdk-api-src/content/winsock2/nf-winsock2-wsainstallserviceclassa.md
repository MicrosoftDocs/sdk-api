---
UID: NF:winsock2.WSAInstallServiceClassA
title: WSAInstallServiceClassA function
author: windows-sdk-content
description: The WSAInstallServiceClass function registers a service class schema within a namespace.
old-location: winsock\wsainstallserviceclass_2.htm
old-project: WinSock
ms.assetid: 06760319-aeeb-4ad7-b77a-01efea7ed904
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: WSAInstallServiceClass, WSAInstallServiceClass function [Winsock], WSAInstallServiceClassA, WSAInstallServiceClassW, _win32_wsainstallserviceclass_2, winsock.wsainstallserviceclass_2, winsock2/WSAInstallServiceClass, winsock2/WSAInstallServiceClassA, winsock2/WSAInstallServiceClassW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
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
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAInstallServiceClassA function


## -description



			The 
<b>WSAInstallServiceClass</b> function registers a service class schema within a namespace. This schema includes the class name, class identifier, and any namespace-specific information that is common to all instances of the service, such as the SAP identifier or object identifier.


## -parameters




### -param lpServiceClassInfo [in]

Service class to namespace specific–type mapping information. Multiple mappings can be handled at one time. 




See the section 
<a href="name_resolution_data_structures_2.htm">Service Class Data Structures</a> for a description of pertinent data structures.


## -returns



The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_PARAMETER</a></b></dt>
</dl>
</td>
<td width="60%">
The namespace provider cannot supply the requested class information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling function does not have sufficient privileges to install the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
Service class information has already been registered for this service class identifier. To modify service class information, first use 
<a href="https://msdn.microsoft.com/7d72f727-cca9-4a07-beb4-d64f23c1f0c1">WSARemoveServiceClass</a>, and then reinstall with updated class information data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The service class information was not valid or improperly structured. This error is returned if the <i>lpServiceClassInfo</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The requested name is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>



<a href="https://msdn.microsoft.com/e177bb7d-c7d3-43a4-a809-ab8212feea2e">WSAGetServiceClassInfo</a>



<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFO</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

