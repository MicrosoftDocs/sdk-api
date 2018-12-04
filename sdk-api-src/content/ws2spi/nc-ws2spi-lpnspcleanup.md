---
UID: NC:ws2spi.LPNSPCLEANUP
title: LPNSPCLEANUP
author: windows-sdk-content
description: Terminates the use of a particular Windows Sockets namespace service provider.
old-location: winsock\nspcleanup_2.htm
tech.root: winsock
ms.assetid: bef888a2-7cfd-4096-bd03-e1864af42365
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: LPNSPCLEANUP, NSPCleanup, NSPCleanup function [Winsock], _win32_nspcleanup_2, winsock.nspcleanup_2, ws2spi/NSPCleanup
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
 - NSPCleanup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPNSPCLEANUP callback function


## -description


The 
<b>NSPCleanup</b> function terminates the use of a particular Windows Sockets namespace service provider.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the namespace provider to be terminated.


## -returns



If no error occurs, 
<b>NSPCleanup</b> returns a value of <b>NO_ERROR</b> (zero). Otherwise, <b>SOCKET_ERROR</b> (–1) is returned and the provider must set the appropriate error code using <a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter does not specify a valid provider.

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
</table>
 




## -remarks



The 
<b>NSPCleanup</b> function is called when an application is finished using a Windows Sockets namespace service provider. The 
<b>NSPCleanup</b> function deregisters a particular namespace provider and allows the transport service provider to free any of the namespace provider's allocated resources.

The 
<a href="https://msdn.microsoft.com/ed9e4ff3-736a-4037-bf85-5572f0cd279d">NSPStartup</a> function must be called successfully before using any namespace providers. It is permissible to make more than one 
<b>NSPStartup</b> call. However, for each 
<b>NSPStartup</b> call, a corresponding 
<b>NSPCleanup</b> call must also be issued. Only the final 
<b>NSPCleanup</b> for the service provider does the actual cleanup; the preceding calls decrement an internal reference count in the service provider.

This function should not return until the namespace service provider DLL can be unloaded from memory.




## -see-also




<a href="https://msdn.microsoft.com/ed9e4ff3-736a-4037-bf85-5572f0cd279d">NSPStartup</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

