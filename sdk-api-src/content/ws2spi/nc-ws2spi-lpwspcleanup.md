---
UID: NC:ws2spi.LPWSPCLEANUP
title: LPWSPCLEANUP
description: The LPWSPCleanup function terminates use of the Windows Sockets service provider.
ms.date: 9/12/2019
ms.keywords: LPWSPCLEANUP
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - ws2spi.h
api_name:
 - LPWSPCLEANUP
---

## -description
The <b>LPWSPCleanup</b> function terminates use of the Windows Sockets service provider.

## -parameters

### -param lpErrno [out]
Pointer to the error code.

## -returns
The return value is zero if the operation has been successfully initiated. Otherwise, the value SOCKET_ERROR is returned, and a specific error number is available in <i>lpErrno</i>.

<table>
<tr>
<th> Error Code </th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSANOTINITIALISED">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nf-ws2spi-wspstartup"><b>WSPStartup</b></a> call must occur before using this function.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Provider identifier given to the name-space provider is not managed by the name-space provider.
</td>
</tr>
</table>

## -remarks
The Windows Sockets 2 SPI client is required to perform a successful <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nf-ws2spi-wspstartup"><b>WSPStartup</b></a> call before it can use Winsock service providers. When it has completed the use of Winsock service providers, the SPI client will call <b>LPWSPCleanup</b> to deregister itself from a Winsock service provider and allow the service provider to free any resources allocated on behalf of the Windows Sockets 2 client. It is permissible for SPI clients to make more than one <b>WSPStartup</b> call. For each <b>WSPStartup</b> call, a corresponding <b>LPWSPCleanup</b> call will also be issued. Only the final <b>LPWSPCleanup</b> for the service provider does the actual cleanup; the preceding calls simply decrement an internal reference count in the Winsock service provider.

When the internal reference count reaches zero and actual cleanup operations commence, any pending blocking or asynchronous calls issued by any thread in this process are canceled without posting any notification messages or signaling any event objects. Any pending overlapped send and receive operations (<a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend"><b>LPWSPSend</b></a>, <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto"><b>LPWSPSendTo</b></a>, <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv"><b>LPWSPRecv</b></a>, <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom"><b>LPWSPRecvFrom</b></a> with an overlapped socket) issued by any thread in this process are also canceled without setting the event object or invoking the completion routine, if specified. In this case, the pending overlapped operations fail with the error status WSA_OPERATION_ABORTED. Any sockets open when <b>LPWSPCleanup</b> is called are reset and automatically deallocated as if <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket"><b>LPWSPCloseSocket</b></a> was called; sockets that have been closed with <b>LPWSPCloseSocket</b> but still have pending data to be sent are not affected, but the pending data is still sent.

This function should not return until the service provider DLL is prepared to be unloaded from memory. In particular, any data remaining to be transmitted must either already have been sent or be queued for transmission by portions of the transport stack that will not be unloaded from memory along with the service provider's DLL.

A Winsock service provider must be prepared to deal with a process that terminates without invoking <b>LPWSPCleanup</b> (for example, as a result of an error). A Winsock service provider must ensure that <b>LPWSPCleanup</b> leaves things in a state in which the Ws2_32.dll can immediately invoke <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nf-ws2spi-wspstartup"><b>WSPStartup</b></a> to reestablish Winsock usage.

## -see-also
<a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a>

<a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a>

<a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>