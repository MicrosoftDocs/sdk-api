---
UID: NF:winsock2.WSAProviderConfigChange
title: WSAProviderConfigChange function (winsock2.h)
description: The WSAProviderConfigChange function notifies the application when the provider configuration is changed.
helpviewer_keywords: ["WSAProviderConfigChange","WSAProviderConfigChange function [Winsock]","_win32_wsaproviderconfigchange_2","winsock.wsaproviderconfigchange_2","winsock2/WSAProviderConfigChange"]
old-location: winsock\wsaproviderconfigchange_2.htm
tech.root: WinSock
ms.assetid: abaf367a-8f99-478c-a58c-d57e9f9cd8a1
ms.date: 12/05/2018
ms.keywords: WSAProviderConfigChange, WSAProviderConfigChange function [Winsock], _win32_wsaproviderconfigchange_2, winsock.wsaproviderconfigchange_2, winsock2/WSAProviderConfigChange
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - WSAProviderConfigChange
 - winsock2/WSAProviderConfigChange
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
 - WSAProviderConfigChange
---

# WSAProviderConfigChange function


## -description

The 
<b>WSAProviderConfigChange</b> function notifies the application when the provider configuration is changed.

## -parameters

### -param lpNotificationHandle [in, out]

Pointer to notification handle. If the notification handle is set to <b>NULL</b> (the handle value not the pointer itself), this function returns a notification handle in the location pointed to by <i>lpNotificationHandle</i>.

### -param lpOverlapped [in]

Pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](./nc-winsock2-lpwsaoverlapped_completion_routine.md)

Pointer to the completion routine called when the provider change notification is received.

## -returns

If no error occurs the 
<b>WSAProviderConfigChange</b> returns 0. Otherwise, a value of SOCKET_ERROR is returned and a specific error code may be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>. The error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a> indicates that the overlapped operation has been successfully initiated and that completion (and thus change event) will be indicated at a later time.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
Not enough free memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
Value pointed by <i>lpNotificationHandle</i> parameter is not a valid notification handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
Current operating system environment does not support provider installation or removal without restart.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAProviderConfigChange</b> function notifies the application of provider (both transport and namespace) installation or removal in Windows operating environments that support such configuration change without requiring a restart. When called for the first time (<i>lpNotificationHandle</i> parameter points to <b>NULL</b> handle), this function completes immediately and returns notification handle in the location pointed by <i>lpNotificationHandle</i> that can be used in subsequent calls to receive notifications of provider installation and removal. The second and any subsequent calls only complete when provider information changes since the time the call was made It is expected (but not required) that the application uses overlapped I/O on second and subsequent calls to 
<b>WSAProviderConfigChange</b>, in which case the call will return immediately and application will be notified of provider configuration changes using the completion mechanism chosen through specified overlapped completion parameters.

Notification handle returned by 
<b>WSAProviderConfigChange</b> is like any regular operating system handle that should be closed (when no longer needed) using Windows 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> call.

The following sequence of actions can be used to guarantee that application always has current protocol configuration information:

<ul>
<li>Call <b>WSAProviderConfigChange</b></li>
<li>Call 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> and/or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>
</li>
<li>Whenever 
<b>WSAProviderConfigChange</b> notifies application of provider configuration change (through blocking or overlapped I/O), the whole sequence of actions should be repeated.</li>
</ul>
<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>