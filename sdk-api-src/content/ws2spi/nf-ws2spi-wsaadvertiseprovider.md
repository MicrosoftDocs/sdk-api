---
UID: NF:ws2spi.WSAAdvertiseProvider
title: WSAAdvertiseProvider function (ws2spi.h)
description: Makes a specific namespace version-2 provider available for all eligible clients.
helpviewer_keywords: ["WSAAdvertiseProvider","WSAAdvertiseProvider function [Winsock]","winsock.wsaadvertiseprovider","ws2spi/WSAAdvertiseProvider"]
old-location: winsock\wsaadvertiseprovider.htm
tech.root: WinSock
ms.assetid: 574ebfa4-d7f2-43c2-b1ec-35ce3db9151f
ms.date: 12/05/2018
ms.keywords: WSAAdvertiseProvider, WSAAdvertiseProvider function [Winsock], winsock.wsaadvertiseprovider, ws2spi/WSAAdvertiseProvider
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
 - WSAAdvertiseProvider
 - ws2spi/WSAAdvertiseProvider
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
 - WSAAdvertiseProvider
---

# WSAAdvertiseProvider function


## -description

The 
**WSAAdvertiseProvider** function makes a specific namespace version-2 provider available for all eligible clients.

## -parameters

### -param puuidProviderId [in]

A pointer to the provider ID of the namespace provider to be advertised.

### -param pNSPv2Routine [in]

A pointer to a **NSPV2_ROUTINE** structure with the namespace service provider version-2 entry points supported by the provider.

## -returns

If no error occurs, 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaprovidercompleteasynccall">WSAProviderCompleteAsyncCall</a> returns zero.

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
A parameter was not valid. This error is returned if the <i>puuidProviderId</i> or <i>pNSPv2Routine</i> parameters were **NULL**. 

This error is also returned if the **NSPv2LookupServiceBegin**, **NSPv2LookupServiceNextEx**, or **NSPv2LookupServiceEnd** members of the **NSPV2_ROUTINE** structure pointed to by the <i>pNSPv2Routine</i> parameter are **NULL**. A namespace version-2 provider must at least support name resolution which this minimum set of functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVALIDPROVIDER</a></b></dl>
</dl>
</td>
<td width="60%">
The namespace provider could not be found for the specified <i>puuidProviderId</i> parameter.

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
**WSAAdvertiseProvider** function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the **WSAAdvertiseProvider** function can only be used for operations on NS_EMAIL namespace providers.

The 
**WSAAdvertiseProvider** function advertises an instance of a NSPv2 provider for clients to find. If the instance to be advertised is an instance of an application-type provider (a namespace provider where the **dwProvideType** member of the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure is **ProviderType_Application**), the advertised provider instance will be visible to all the client processes running under the same user and in the same session as the caller of **WSAAdvertiseProvider**. 

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as a result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the **WSAAdvertiseProvider** and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a> functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).

The 
**WSAAdvertiseProvider** function is called by any application that wants to make a specific provider available for all eligible clients (currently all the applications running with the same credentials as the hosting application, and in the same user session). 



A process can implement and advertise multiple providers at the same time. Windows Sockets will manage the namespace providers by dispatching calls to the correct one. It will also hide RPC interface details and translates cross-process calls into in-process calls. So that the NSPv2 provider has only to implement a table of entry point functions similar to the <a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a> structure used by an NSPv1 provider. A NSPv2 provider does not have to worry about RPC specific requirements (data marshalling and serialization, for example).



The **WSAAdvertiseProvider** caller passes a pointer to an <a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>  structure in the <i>pNSPv2Routine</i> parameter with the NSPv2 entry points supported by the provider. 


The 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a> function makes a specific namespace provider no longer available for clients.

## -see-also

<a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="/windows/desktop/api/nsemail/ne-nsemail-napi_provider_type">NAPI_PROVIDER_TYPE</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaprovidercompleteasynccall">WSAProviderCompleteAsyncCall</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea">WSASetService</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaunadvertiseprovider">WSAUnadvertiseProvider</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>

