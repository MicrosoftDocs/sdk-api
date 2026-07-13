---
UID: NF:winsock2.WSAEnumNameSpaceProvidersExW
title: WSAEnumNameSpaceProvidersExW function (winsock2.h)
description: Retrieves information on available namespace providers. (Unicode)
helpviewer_keywords: ["WSAEnumNameSpaceProvidersEx", "WSAEnumNameSpaceProvidersEx function [Winsock]", "WSAEnumNameSpaceProvidersExW", "winsock.wsaenumnamespaceprovidersex", "winsock2/WSAEnumNameSpaceProvidersEx", "winsock2/WSAEnumNameSpaceProvidersExW"]
old-location: winsock\wsaenumnamespaceprovidersex.htm
tech.root: WinSock
ms.assetid: 34bc96aa-63f7-4ab8-9376-6f4b979225ca
ms.date: 12/05/2018
ms.keywords: WSAEnumNameSpaceProvidersEx, WSAEnumNameSpaceProvidersEx function [Winsock], WSAEnumNameSpaceProvidersExA, WSAEnumNameSpaceProvidersExW, winsock.wsaenumnamespaceprovidersex, winsock2/WSAEnumNameSpaceProvidersEx, winsock2/WSAEnumNameSpaceProvidersExA, winsock2/WSAEnumNameSpaceProvidersExW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAEnumNameSpaceProvidersExW (Unicode) and WSAEnumNameSpaceProvidersExA (ANSI)
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
 - WSAEnumNameSpaceProvidersExW
 - winsock2/WSAEnumNameSpaceProvidersExW
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
 - WSAEnumNameSpaceProvidersEx
 - WSAEnumNameSpaceProvidersExA
 - WSAEnumNameSpaceProvidersExW
---

# WSAEnumNameSpaceProvidersExW function


## -description

The 
<b>WSAEnumNameSpaceProvidersEx</b> function retrieves information on available namespace providers.

## -parameters

### -param lpdwBufferLength [in, out]

On input, the number of bytes contained in the buffer pointed to by <i>lpnspBuffer</i>. On output (if the function fails, and the error is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a>), the minimum number of bytes to allocate for the <i>lpnspBuffer</i> buffer to allow it to retrieve all the requested information. The buffer passed to <b>WSAEnumNameSpaceProvidersEx</b> must be sufficient to hold all of the namespace information.

### -param lpnspBuffer [out]

A buffer that is filled with 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEX</a> structures. The returned structures are located consecutively at the head of the buffer. Variable sized information referenced by pointers in the structures point to locations within the buffer located between the end of the fixed sized structures and the end of the buffer. The number of structures filled in is the return value of 
<b>WSAEnumNameSpaceProvidersEx</b>.

## -returns

The 
<b>WSAEnumNameSpaceProvidersEx</b> function returns the number of 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEX</a> structures copied into <i>lpnspBuffer</i>. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpnspBuffer</i> parameter was a <b>NULL</b> pointer or the buffer length, <i>lpdwBufferLength</i>, was too small to receive all the relevant 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEX</a> structures and associated information. When this error is returned, the buffer length required is returned in the <i>lpdwBufferLength</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>

## -remarks

The <b>WSAEnumNameSpaceProvidersEx</b>  function is an enhanced version of the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a> function. The provider-specific data blob associated with the namespace entry
                     passed in the <i>lpProviderInfo</i> parameter to the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a> function can be queried using <b>WSAEnumNameSpaceProvidersEx</b> function. 

Currently, the only namespace provider included with Windows that sets information in the <b>ProviderSpecific</b> member of the  <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEX</a> structure is the NS_EMAIL provider. The format of the <b>ProviderSpecific</b> member for an NS_EMAIL namespace provider is a <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure. 

When UNICODE or _UNICODE is defined, <b>WSAEnumNameSpaceProvidersEx</b> is defined to <b>WSAEnumNameSpaceProvidersExW</b>, the Unicode version of this function. The <i>lpnspBuffer</i> parameter is defined to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">LPSAWSANAMESPACE_INFOEXW</a> data type and <b>WSANAMESPACE_INFOEXW</b> structures are returned on success.

When UNICODE or _UNICODE is not defined, <b>WSAEnumNameSpaceProvidersEx</b> is defined to <b>WSAEnumNameSpaceProvidersExA</b>, the ANSI version of this function. The <i>lpnspBuffer</i> parameter is defined to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">LPSAWSANAMESPACE_INFOEXA</a> data type and <b>WSANAMESPACE_INFOEXA</b> structures are returned on success.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The  <b>WSAEnumNameSpaceProvidersExW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSAEnumNameSpaceProvidersEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEX</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx32</a>
