---
UID: NC:ws2spi.LPNSPV2STARTUP
title: LPNSPV2STARTUP (ws2spi.h)
description: Notifies a namespace service provider version-2 (NSPv2) provider that a new client process is to begin using the provider.
helpviewer_keywords: ["LPNSPV2STARTUP","NSPv2Startup","NSPv2Startup function [Winsock]","winsock.nspv2startup","ws2spi/NSPv2Startup"]
old-location: winsock\nspv2startup.htm
tech.root: WinSock
ms.assetid: 93224e66-9c94-4b5c-af11-ae988b74bc03
ms.date: 12/05/2018
ms.keywords: LPNSPV2STARTUP, NSPv2Startup, NSPv2Startup function [Winsock], winsock.nspv2startup, ws2spi/NSPv2Startup
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNSPV2STARTUP
 - ws2spi/LPNSPV2STARTUP
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
 - NSPv2Startup
---

# LPNSPV2STARTUP callback function


## -description

The 
**NSPv2Startup** function notifies a namespace service provider version-2 (NSPv2) provider that a new client process is to begin using the provider.

## -parameters

### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider to notify.

### -param ppvClientSessionArg [in]

A pointer to the client session.

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (that is, 1) if the routine fails and it must set the appropriate error code using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



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
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dl>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to initialize the service.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a></b></dl>
</dl>
</td>
<td width="60%">
Service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
</table>

## -remarks

The 
**NSPv2Startup** function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the **NSPv2Startup** function can only be used for operations on NS_EMAIL namespace providers.

The 
**NSPv2Startup** function is called each time a new client process begins using namespace provider.  Providers may use the 
client session argument pointed to by the <i>ppvClientSessionArg</i> parameter to store information about this session. The value in the <i>ppvClientSessionArg</i> parameter will be passed to subsequent NSPv2 function calls in the same session. The client session argument may **NULL**, if the namespace provider does not require this information. 

The **NSPv2Startup** function is called when a new client session initializes. 
The **NSPv2Startup** and 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a> functions must be called as pairs. 

The 
**NSPv2Startup** function must be called successfully before calling the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a> function. It is permissible to make more than one 
**NSPv2Startup** call. However, for each 
**NSPv2Startup** call, a corresponding 
**NSPv2Cleanup** call must also be issued. Only the final 
**NSPv2Cleanup** for the service provider does the actual cleanup; the preceding calls decrement an internal reference count in the namespace service provider.

The **NSPv2Startup**,  <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2clientsessionrundown">NSPv2ClientSessionRundown</a>, and  <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a> functions are optional, dependent on the requirements of the NSPv2 provider.

 If the **NSPv2Startup** function isn't implemented, then calls to that function should be intercepted by a stub function that returns <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a>.  The NSPv2 function pointer to the unimplemented **NSPv2Startup** function in the <a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a> structure should point be to the stub function.

## -see-also

<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2clientsessionrundown">NSPv2ClientSessionRundown</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupserviceend">NSPv2LookupServiceEnd</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2setserviceex">NSPv2SetServiceEx</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

