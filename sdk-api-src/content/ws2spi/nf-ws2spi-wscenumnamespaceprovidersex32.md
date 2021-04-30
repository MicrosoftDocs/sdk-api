---
UID: NF:ws2spi.WSCEnumNameSpaceProvidersEx32
title: WSCEnumNameSpaceProvidersEx32 function (ws2spi.h)
description: Retrieves information on available 32-bit namespace providers.
helpviewer_keywords: ["WSCEnumNameSpaceProvidersEx32","WSCEnumNameSpaceProvidersEx32 function [Winsock]","winsock.wscenumnamespaceprovidersex32","ws2spi/WSCEnumNameSpaceProvidersEx32"]
old-location: winsock\wscenumnamespaceprovidersex32.htm
tech.root: WinSock
ms.assetid: 544120b2-7575-4deb-8429-2bd4582eceef
ms.date: 12/05/2018
ms.keywords: WSCEnumNameSpaceProvidersEx32, WSCEnumNameSpaceProvidersEx32 function [Winsock], winsock.wscenumnamespaceprovidersex32, ws2spi/WSCEnumNameSpaceProvidersEx32
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
 - WSCEnumNameSpaceProvidersEx32
 - ws2spi/WSCEnumNameSpaceProvidersEx32
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
 - WSCEnumNameSpaceProvidersEx32
---

# WSCEnumNameSpaceProvidersEx32 function


## -description

The 
**WSCEnumNameSpaceProvidersEx32** function retrieves information on available 32-bit namespace providers.

## -parameters

### -param lpdwBufferLength [in, out]

On input, the number of bytes contained in the buffer pointed to by <i>lpnspBuffer</i>. On output (if the function fails, and the error is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a>), the minimum number of bytes to allocate for the <i>lpnspBuffer</i> buffer to allow it to retrieve all the requested information. The buffer passed to **WSCEnumNameSpaceProvidersEx32** must be sufficient to hold all of the namespace information.

### -param lpnspBuffer [out]

A buffer that is filled with 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEXW</a> structures. The returned structures are located consecutively at the head of the buffer. Variable sized information referenced by pointers in the structures point to locations within the buffer located between the end of the fixed sized structures and the end of the buffer. The number of structures filled in is the return value of 
**WSCEnumNameSpaceProvidersEx32**.

## -returns

The 
**WSCEnumNameSpaceProvidersEx32** function returns the number of 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEXW</a> structures copied into <i>lpnspBuffer</i>. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The buffer length was too small to receive all the relevant 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEXW</a> structures and associated information or the <i>lpnspBuffer</i> parameter was a **NULL** pointer. When this error is returned, the buffer length required is returned in the <i>lpdwBufferLength</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dl>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
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
</table>

## -remarks

**WSCEnumNameSpaceProvidersEx32** is a strictly 32-bit version of <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

  Currently, the only namespace included with Windows that uses information in the **ProviderSpecific** member of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEXW</a> structure are namespace providers for the NS_EMAIL namespace. The format of the **ProviderSpecific** member for an NS_EMAIL namespace provider is a <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure.

The 32-bit SPI function is equivalent to the native API function (<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>) because there is no concept of a "hidden" namespace provider.

The provider-specific data blob associated with namespace entry
                     passed in the <i>lpProviderInfo</i> parameter to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a> function can be queried using **WSCEnumNameSpaceProvidersEx32** function.

## -see-also

<a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEXW</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceproviders32">WSCEnumNameSpaceProviders32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a>

