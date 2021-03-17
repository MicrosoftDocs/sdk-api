---
UID: NF:ws2spi.WSAProviderCompleteAsyncCall
title: WSAProviderCompleteAsyncCall function (ws2spi.h)
description: Notifies a client when an asynchronous call to a namespace version-2 provider is completed.
helpviewer_keywords: ["WSAProviderCompleteAsyncCall","WSAProviderCompleteAsyncCall function [Winsock]","winsock.wsaprovidercompleteasynccall","ws2spi/WSAProviderCompleteAsyncCall"]
old-location: winsock\wsaprovidercompleteasynccall.htm
tech.root: WinSock
ms.assetid: 2bbc20ae-ad6d-47f6-8ca9-dd5559236fbe
ms.date: 12/05/2018
ms.keywords: WSAProviderCompleteAsyncCall, WSAProviderCompleteAsyncCall function [Winsock], winsock.wsaprovidercompleteasynccall, ws2spi/WSAProviderCompleteAsyncCall
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WSAProviderCompleteAsyncCall
 - ws2spi/WSAProviderCompleteAsyncCall
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
 - WSAProviderCompleteAsyncCall
---

# WSAProviderCompleteAsyncCall function


## -description

The 
**WSAProviderCompleteAsyncCall** function notifies a client when an asynchronous call to a namespace version-2 provider is completed.

## -parameters

### -param hAsyncCall

The handle passed to the asynchronous call being completed. This handle is passed by the client to the namespace version-2 provider in the asynchronous function call.

### -param iRetCode

The return code for the asynchronous call to the namespace version-2 provider.

## -returns

If no error occurs, 
**WSAProviderCompleteAsyncCall** returns zero.

If the function fails, the return value is SOCKET_ERROR. To get extended error information, call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>, which returns one of the following extended error values.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
An internal error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
A parameter was not valid. This error is returned if the <i>hAsyncCall</i> parameter was **NULL**. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>Ws2_32.dll</i> has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
</table>

## -remarks

The 
**WSAProviderCompleteAsyncCall** function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a> function can only be used for operations on NS_EMAIL namespace providers. Asynchronous calls to NSPv2 providers are not supported on Windows Vista and Windows Server 2008. So the **WSAProviderCompleteAsyncCall** is not currently applicable. This function is planned for use in later versions of Windows when asynchronous calls to namespace providers are supported. 

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaadvertiseprovider">WSAAdvertiseProvider</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a> functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).

## -see-also

<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaadvertiseprovider">WSAAdvertiseProvider</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a>

