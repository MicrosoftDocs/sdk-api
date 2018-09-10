---
UID: NC:ws2spi.LPNSPINSTALLSERVICECLASS
title: LPNSPINSTALLSERVICECLASS
author: windows-sdk-content
description: The NSPInstallServiceClass function registers service class schema within the namespace providers.
old-location: winsock\nspinstallserviceclass_2.htm
tech.root: WinSock
ms.assetid: 437a3580-e296-4f20-8921-84e522cccc1a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LPNSPINSTALLSERVICECLASS, NSPInstallServiceClass, NSPInstallServiceClass function [Winsock], _win32_nspinstallserviceclass_2, winsock.nspinstallserviceclass_2, ws2spi/NSPInstallServiceClass
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPInstallServiceClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPNSPINSTALLSERVICECLASS callback function


## -description


The 
<b>NSPInstallServiceClass</b> function registers service class schema within the namespace providers.

The schema includes the class name, class identifier, and any namespace-specific type information that is common to all instances of the service, such as SAP identifier or object identifier. A dynamic namespace provider is expected to store any class information associated with that namespace.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider that this service class schema is registered in.


### -param lpServiceClassInfo [in]

A pointer to the service class schema information.


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
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
The service class information has already been registered for this service class identifier. To modify service class information, first call <a href="https://msdn.microsoft.com/97313e6f-ec9e-4dcb-b888-14436259a519">NSPRemoveServiceClass</a>, then reinstall with updated class information data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The service class identifier was invalid or improperly structured. This error is returned if the <i>lpServiceClassInfo</i> parameter is <b>NULL</b>.

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
</table>
 




## -remarks



Namespace providers are encouraged, but not required, to store information that is specific to the namespace they support.




## -see-also




<a href="https://msdn.microsoft.com/babe1c96-9077-4d91-a52a-839c89d7a83b">NSPGetServiceClassInfo</a>



<a href="https://msdn.microsoft.com/97313e6f-ec9e-4dcb-b888-14436259a519">NSPRemoveServiceClass</a>



<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFOW</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

