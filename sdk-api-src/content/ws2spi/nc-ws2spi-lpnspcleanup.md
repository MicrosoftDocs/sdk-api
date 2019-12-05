---
UID: NC:ws2spi.LPNSPCLEANUP
title: LPNSPCLEANUP (ws2spi.h)
description: Terminates the use of a particular Windows Sockets namespace service provider.
old-location: winsock\nspcleanup_2.htm
tech.root: WinSock
ms.assetid: bef888a2-7cfd-4096-bd03-e1864af42365
ms.date: 12/05/2018
ms.keywords: LPNSPCLEANUP, NSPCleanup, NSPCleanup function [Winsock], _win32_nspcleanup_2, winsock.nspcleanup_2, ws2spi/NSPCleanup
ms.topic: callback
f1_keywords:
- ws2spi/NSPCleanup
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPNSPCLEANUP callback function


## -description


The 
**NSPCleanup** function terminates the use of a particular Windows Sockets namespace service provider.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the namespace provider to be terminated.


## -returns



If no error occurs, 
**NSPCleanup** returns a value of **NO_ERROR** (zero). Otherwise, **SOCKET_ERROR** (–1) is returned and the provider must set the appropriate error code using <a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter does not specify a valid provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>[WSAEOPNOTSUPP](https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP)</b></dl>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
</table>
 




## -remarks



The 
**NSPCleanup** function is called when an application is finished using a Windows Sockets namespace service provider. The 
**NSPCleanup** function deregisters a particular namespace provider and allows the transport service provider to free any of the namespace provider's allocated resources.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-nspstartup">NSPStartup</a> function must be called successfully before using any namespace providers. It is permissible to make more than one 
**NSPStartup** call. However, for each 
**NSPStartup** call, a corresponding 
**NSPCleanup** call must also be issued. Only the final 
**NSPCleanup** for the service provider does the actual cleanup; the preceding calls decrement an internal reference count in the service provider.

This function should not return until the namespace service provider DLL can be unloaded from memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-nspstartup">NSPStartup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>
 

 

