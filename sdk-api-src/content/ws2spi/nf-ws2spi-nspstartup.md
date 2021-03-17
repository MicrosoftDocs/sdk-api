---
UID: NF:ws2spi.NSPStartup
title: NSPStartup function (ws2spi.h)
description: Retrieves the dynamic information about a provider, such as the list of the DLL entry points.
helpviewer_keywords: ["NSPStartup","NSPStartup function [Winsock]","_win32_nspstartup_2","winsock.nspstartup_2","ws2spi/NSPStartup"]
old-location: winsock\nspstartup_2.htm
tech.root: WinSock
ms.assetid: ed9e4ff3-736a-4037-bf85-5572f0cd279d
ms.date: 12/05/2018
ms.keywords: NSPStartup, NSPStartup function [Winsock], _win32_nspstartup_2, winsock.nspstartup_2, ws2spi/NSPStartup
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NSPStartup
 - ws2spi/NSPStartup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPStartup
---

# NSPStartup function


## -description

The 
**NSPStartup** function retrieves the dynamic information about a provider, such as the list of the DLL entry points.

This function is called by the client upon initialization. 
The **NSPStartup** and 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspcleanup">NSPCleanup</a> functions must be called as pairs. All  NSP functions must be called from within an **NSPStartup**/**NSPCleanup** pair. It is not required that WSC functions be called from within a **NSPStartup**/**NSPCleanup** pair.

## -parameters

### -param lpProviderId [in]

The desired provider from which to return the entry points.

### -param lpnspRoutines [out]

A pointer to an <a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a> structure that points to provider entry points if the function call is successful.

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (–1) if the function fails and it must set the appropriate error code using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVALIDPROCTABLE</a></b></dl>
</dl>
</td>
<td width="60%">
The procedure call table is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></b></dl>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASYSNOTREADY</a></b></dl>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/ws2spi/nf-ws2spi-nspstartup">NSPStartup</a> function cannot operate at this time because the underlying system it uses to provide network services is currently unavailable.

</td>
</tr>
</table>

## -remarks

For more information, see the <a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a> structure.

## -see-also

<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspcleanup">NSPCleanup</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

