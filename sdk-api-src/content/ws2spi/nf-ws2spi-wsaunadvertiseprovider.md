---
UID: NF:ws2spi.WSAUnadvertiseProvider
title: WSAUnadvertiseProvider function (ws2spi.h)
description: Makes a specific namespace version-2 provider no longer available for clients.
helpviewer_keywords: ["WSAUnadvertiseProvider","WSAUnadvertiseProvider function [Winsock]","winsock.wsaunadvertiseprovider","ws2spi/WSAUnadvertiseProvider"]
old-location: winsock\wsaunadvertiseprovider.htm
tech.root: WinSock
ms.assetid: 5975b496-53a7-4f8a-8efc-27ef447596c2
ms.date: 12/05/2018
ms.keywords: WSAUnadvertiseProvider, WSAUnadvertiseProvider function [Winsock], winsock.wsaunadvertiseprovider, ws2spi/WSAUnadvertiseProvider
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
 - WSAUnadvertiseProvider
 - ws2spi/WSAUnadvertiseProvider
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
 - WSAUnadvertiseProvider
---

# WSAUnadvertiseProvider function


## -description

The 
**WSAUnadvertiseProvider** function makes a specific namespace version-2 provider no longer available for clients.

## -parameters

### -param puuidProviderId [in]

A pointer to the provider ID of the namespace provider.

## -returns

If no error occurs, 
**WSAUnadvertiseProvider** returns zero. Otherwise, it returns **SOCKET_ERROR**, and a specific error code is available by calling <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
A parameter was not valid. This error is returned if the <i>puuidProviderId</i> parameter was **NULL**. 

</td>
</tr>
</table>

## -remarks

The 
**WSAUnadvertiseProvider** function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the **WSAUnadvertiseProvider** function can only be used for operations on NS_EMAIL namespace providers.

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaadvertiseprovider">WSAAdvertiseProvider</a> and **WSAUnadvertiseProvider** functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).

## -see-also

<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wsaadvertiseprovider">WSAAdvertiseProvider</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea">WSASetService</a>

