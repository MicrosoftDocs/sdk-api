---
UID: NF:ws2spi.WSCEnumNameSpaceProviders32
title: WSCEnumNameSpaceProviders32 function (ws2spi.h)
description: Returns information on available 32-bit namespace providers.Note  This call is a strictly 32-bit version of WSAEnumNameSpaceProviders for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs. .
helpviewer_keywords: ["WSCEnumNameSpaceProviders32","WSCEnumNameSpaceProviders32 function [Winsock]","winsock.wscenumnamespaceproviders32","ws2spi/WSCEnumNameSpaceProviders32"]
old-location: winsock\wscenumnamespaceproviders32.htm
tech.root: WinSock
ms.assetid: 792737d9-231d-4524-b1a6-b9904951d5b4
ms.date: 12/05/2018
ms.keywords: WSCEnumNameSpaceProviders32, WSCEnumNameSpaceProviders32 function [Winsock], winsock.wscenumnamespaceproviders32, ws2spi/WSCEnumNameSpaceProviders32
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 x64 Edition [desktop apps only]
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
 - WSCEnumNameSpaceProviders32
 - ws2spi/WSCEnumNameSpaceProviders32
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
 - WSCEnumNameSpaceProviders32
---

# WSCEnumNameSpaceProviders32 function


## -description

The **WSCEnumNameSpaceProviders32** function returns information on available 32-bit namespace providers.<div class="alert">**Note**  This call is a strictly 32-bit version of <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a> for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs.</div>
<div> </div>

## -parameters

### -param lpdwBufferLength [in, out]

On input, the number of bytes contained in the buffer pointed to by <i>lpnspBuffer</i>. On output (if the function fails, and the error is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a>), the minimum number of bytes to allocate for the <i>lpnspBuffer</i> buffer to allow it to retrieve all the requested information. The buffer passed to **WSCEnumNameSpaceProviders32** must be sufficient to hold all of the namespace information.

### -param lpnspBuffer [out]

A buffer that is filled with 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFOW</a> structures. The returned structures are located consecutively at the head of the buffer. Variable sized information referenced by pointers in the structures point to locations within the buffer located between the end of the fixed sized structures and the end of the buffer. The number of structures filled in is the return value of 
**WSCEnumNameSpaceProviders32**.

## -returns

The 
**WSCEnumNameSpaceProviders32** function returns the number of 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFOW</a> structures copied into <i>lpnspBuffer</i>. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
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
The <i>lpnspBuffer</i> parameter was a **NULL** pointer or the buffer length, <i>lpdwBufferLength</i>, was too small to receive all the relevant 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFOW</a> structures and associated information. When this error is returned, the buffer length required is returned in the <i>lpdwBufferLength</i> parameter. 

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

**WSCEnumNameSpaceProviders32** is a strictly 32-bit version of <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The 32-bit SPI function is equivalent to the native API function (<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>) because there is no concept of a "hidden" namespace provider.

The **WSCEnumNameSpaceProviders32** function is a Unicode only function and returns <a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infoexw">WSANAMESPACE_INFOEXW</a> structures.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanamespace_infow">WSANAMESPACE_INFOW</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace32">WSCInstallNameSpace32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx32</a>

