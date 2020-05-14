---
UID: NC:ws2spi.LPNSPV2CLIENTSESSIONRUNDOWN
title: LPNSPV2CLIENTSESSIONRUNDOWN (ws2spi.h)
description: Notifies a namespace service provider version-2 (NSPv2) provider that the client session is terminating.helpviewer_keywords: ["LPNSPV2CLIENTSESSIONRUNDOWN","NSPv2ClientSessionRundown","NSPv2ClientSessionRundown function [Winsock]","winsock.nspv2clientsessionrundown","ws2spi/NSPv2ClientSessionRundown"]
old-location: winsock\nspv2clientsessionrundown.htm
tech.root: WinSock
ms.assetid: 7379b502-129a-4dac-b7eb-e6fae8fb23f8
ms.date: 12/05/2018
ms.keywords: LPNSPV2CLIENTSESSIONRUNDOWN, NSPv2ClientSessionRundown, NSPv2ClientSessionRundown function [Winsock], winsock.nspv2clientsessionrundown, ws2spi/NSPv2ClientSessionRundown
f1_keywords:
- ws2spi/NSPv2ClientSessionRundown
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ws2spi.h
api_name:
- NSPv2ClientSessionRundown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPNSPV2CLIENTSESSIONRUNDOWN callback function


## -description


The 
**NSPv2ClientSessionRundown** function notifies a namespace service provider version-2 (NSPv2) provider that the client session is terminating.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider to notify.


### -param pvClientSessionArg [in]

A pointer to the client session that is terminating. 


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
The calling routine does not have sufficient privileges to install the service.

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
The operation is not supported. This error is returned if the namespace provider does not implement this function. This error can also be returned if the specified <i>dwControlCode</i> is an unrecognized command.

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
**NSPv2ClientSessionRundown** function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the **NSPv2ClientSessionRundown** function can only be used for operations on NS_EMAIL namespace providers.

The 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2startup">NSPv2Startup</a> function is called each time a new client process begins using namespace provider.  Providers may use the 
client session argument pointed to by the <i>ppvClientSessionArg</i> parameter to store information about this session. If a value was specified for the client session argument in the call to the **NSPv2Startup** function, then this same client session argument is passed in the  <i>pvClientSessionArg</i> parameter to the **NSPv2ClientSessionRundown** function.

The <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2startup">NSPv2Startup</a>,  **NSPv2ClientSessionRundown**, and  <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a> functions are optional, dependent on the requirements of the NSPv2 provider.

 If the **NSPv2ClientSessionRundown** function isn't implemented, then calls to that function should be intercepted by a stub function that returns <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a>.  The NSPv2 function pointer to the unimplemented **NSPv2ClientSessionRundown** function in the <a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a> structure should point be to the stub function. 




## -see-also




<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupserviceend">NSPv2LookupServiceEnd</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2setserviceex">NSPv2SetServiceEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2startup">NSPv2Startup</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>
 

 

