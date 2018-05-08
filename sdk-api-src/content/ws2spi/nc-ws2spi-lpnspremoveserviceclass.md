---
UID: NC:ws2spi.LPNSPREMOVESERVICECLASS
title: LPNSPREMOVESERVICECLASS
author: windows-driver-content
description: Permanently removes a specified service class from the namespace.
old-location: winsock\nspremoveserviceclass_2.htm
old-project: WinSock
ms.assetid: 97313e6f-ec9e-4dcb-b888-14436259a519
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: LPNSPREMOVESERVICECLASS, NSPRemoveServiceClass, NSPRemoveServiceClass function [Winsock], _win32_nspremoveserviceclass_2, winsock.nspremoveserviceclass_2, ws2spi/NSPRemoveServiceClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ws2spi.h
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
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ws2spi.h
api_name:
-	NSPRemoveServiceClass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPREMOVESERVICECLASS callback function


## -description



			The 
<b>NSPRemoveServiceClass</b> function permanently removes a specified service class from the namespace.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider that this service class schema is to be removed from.


### -param lpServiceClassId [in]

A pointer to the GUID for the service class to remove.


## -returns




						The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (–1) if the routine fails and it must set the appropriate error code using 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



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
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_PARAMETER</a></b></dt>
</dl>
</td>
<td width="60%">
The specified GUID was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to remove the Service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified service class identifier GUID was not valid.

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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSATYPE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The specified class was not found in any of the namespaces.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

