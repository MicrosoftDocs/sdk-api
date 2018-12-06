---
UID: NF:winsock2.WSAGetServiceClassInfoW
title: WSAGetServiceClassInfoW function
author: windows-sdk-content
description: The WSAGetServiceClassInfo function retrieves the class information (schema) pertaining to a specified service class from a specified namespace provider.
old-location: winsock\wsagetserviceclassinfo_2.htm
tech.root: winsock
ms.assetid: e177bb7d-c7d3-43a4-a809-ab8212feea2e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSAGetServiceClassInfo, WSAGetServiceClassInfo function [Winsock], WSAGetServiceClassInfoA, WSAGetServiceClassInfoW, _win32_wsagetserviceclassinfo_2, winsock.wsagetserviceclassinfo_2, winsock2/WSAGetServiceClassInfo, winsock2/WSAGetServiceClassInfoA, winsock2/WSAGetServiceClassInfoW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a>, this parameter specifies the minimum size, in bytes, of the buffer pointed to <i>lpServiceClassInfo</i> needed to retrieve the record.


### -param lpServiceClassInfo [out]

A pointer to a <a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFO</a> structure that contains the service class information from the indicated namespace provider for the specified service class.


## -returns



The return value is zero if the 
<b>WSAGetServiceClassInfo</b> was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
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
The calling routine does not have sufficient privileges to access the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>lpServiceClassInfo</i> parameter is too small to contain a WSASERVICECLASSINFOW. The application needs to pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified service class identifier or namespace provider identifier is not valid. This error is returned if the <i>lpProviderId</i>, <i>lpServiceClassId</i>, <i>lpdwBufSize</i>, or <i>lpServiceClassInfo</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported for the type of object referenced. This error is returned by some namespace providers that do not support getting service class information.

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
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSATYPE_NOT_FOUND</a></b></dt>
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
<a href="https://msdn.microsoft.com/fb225e0c-a0c7-44e1-80fb-7b924b371afa">Service Class Data Structures</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/fb225e0c-a0c7-44e1-80fb-7b924b371afa">Service Class Data Structures</a>



<a href="https://msdn.microsoft.com/06760319-aeeb-4ad7-b77a-01efea7ed904">WSAInstallServiceClass</a>



<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFOW</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

