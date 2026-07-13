---
UID: NF:winsock2.WSAEnumProtocolsA
title: WSAEnumProtocolsA function (winsock2.h)
description: The WSAEnumProtocols function retrieves information about available transport protocols. (ANSI)
helpviewer_keywords: ["WSAEnumProtocolsA", "winsock2/WSAEnumProtocolsA"]
old-location: winsock\wsaenumprotocols_2.htm
tech.root: WinSock
ms.assetid: 928b6937-41a3-4268-a3bc-14c9e04870e4
ms.date: 12/05/2018
ms.keywords: WSAEnumProtocols, WSAEnumProtocols function [Winsock], WSAEnumProtocolsA, WSAEnumProtocolsW, _win32_wsaenumprotocols_2, winsock.wsaenumprotocols_2, winsock2/WSAEnumProtocols, winsock2/WSAEnumProtocolsA, winsock2/WSAEnumProtocolsW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAEnumProtocolsW (Unicode) and WSAEnumProtocolsA (ANSI)
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
 - WSAEnumProtocolsA
 - winsock2/WSAEnumProtocolsA
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
 - WSAEnumProtocols
 - WSAEnumProtocolsA
 - WSAEnumProtocolsW
---

# WSAEnumProtocolsA function


## -description

The 
<b>WSAEnumProtocols</b> function retrieves information about available transport protocols.

## -parameters

### -param lpiProtocols [in]

A <b>NULL</b>-terminated array of iProtocol values. This parameter is optional; if <i>lpiProtocols</i> is <b>NULL</b>, information on all available protocols is returned. Otherwise, information is retrieved only for those protocols listed in the array.

### -param lpProtocolBuffer [out]

A pointer to a buffer that is filled with 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structures.

### -param lpdwBufferLength [in, out]

On input, number of bytes in the <i>lpProtocolBuffer</i> buffer passed to 
<b>WSAEnumProtocols</b>. On output, the minimum buffer size that can be passed to 
<b>WSAEnumProtocols</b> to retrieve all the requested information. This routine has no ability to enumerate over multiple calls; the passed-in buffer must be large enough to hold all entries in order for the routine to succeed. This reduces the complexity of the API and should not pose a problem because the number of protocols loaded on a computer is typically small.

## -returns

If no error occurs, 
<b>WSAEnumProtocols</b> returns the number of protocols to be reported. Otherwise, a value of SOCKET_ERROR is returned and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Indicates that one of the specified parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer length was too small to receive all the relevant 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structures and associated information. Pass in a buffer at least as large as the value returned in <i>lpdwBufferLength</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the <i>lpiProtocols</i>, <i>lpProtocolBuffer</i>, or <i>lpdwBufferLength</i> parameters are not a valid part of the user address space.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAEnumProtocols</b> function is used to discover information about the collection of transport protocols installed on the local computer. Layered protocols are only usable by applications when installed in protocol chains. Information on layered protocols is not returned except for any dummy layered service providers (LSPs) installed with a chain length of zero in the  <i>lpProtocolBuffer</i>. 

<div class="alert"><b>Note</b>  Layered Service Providers are deprecated. Starting with Windows 8 and Windows Server 2012, use <a href="/windows/desktop/FWP/windows-filtering-platform-start-page">Windows Filtering Platform</a>.</div>
<div> </div>
The <i>lpiProtocols</i> parameter can be used as a filter to constrain the amount of information provided. Often, <i>lpiProtocols</i> will be specified as a <b>NULL</b> pointer that will cause the function to return information on all available transport protocols and protocol chains.

The 
<b>WSAEnumProtocols</b> function differs from the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a> functions in that 
the <b>WSAEnumProtocols</b> function doesn't return <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structures for all installed protocols. The <b>WSAEnumProtocols</b> function excludes protocols that the service provider has set with the <b>PFL_HIDDEN</b> flag in the <b>dwProviderFlags</b> member of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure to indicate to the Ws2_32.dll that this protocol should not be returned in the result buffer generated by <b>WSAEnumProtocols</b> function.  In addition, the <b>WSAEnumProtocols</b> function does not return data for <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structures that have a chain length of one or greater (an LSP provider).   The <b>WSAEnumProtocols</b> only returns information on base protocols and protocol chains that lack the <b>PFL_HIDDEN</b> flag  and don't have a protocol chain length of zero. 

A 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure is provided in the buffer pointed to by <i>lpProtocolBuffer</i> for each requested protocol. If the specified buffer is not large enough (as indicated by the input value of <i>lpdwBufferLength</i> ), the value pointed to by <i>lpdwBufferLength</i> will be updated to indicate the required buffer size. The application should then obtain a large enough buffer and call 
<b>WSAEnumProtocols</b> again.

The order in which the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structures appear in the buffer coincides with the order in which the protocol entries were registered by the service provider using the WS2_32.DLL, or with any subsequent reordering that occurred through the Windows Sockets application or DLL supplied for establishing default TCP/IP providers.

<b>Windows Phone 8:</b> The <b>WSAEnumProtocolsW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSAEnumProtocolsW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

The following example demonstrates the use of the <b>WSAEnumProtocols</b> function to retrieve an array of <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structures for available transport protocols.


```cpp
#ifndef UNICODE
#define UNICODE 1
#endif

#include <winsock2.h>
#include <ws2tcpip.h>
#include <objbase.h>
#include <stdio.h>

// Link with ws2_32.lib and ole32.lib
#pragma comment (lib, "Ws2_32.lib")
#pragma comment (lib, "ole32.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))
// Note: could also use malloc() and free()

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult = 0;

    int iError = 0;
    INT iNuminfo = 0;

    int i;

    // Allocate a 16K buffer to retrieve all the protocol providers
    DWORD dwBufferLen = 16384;

    LPWSAPROTOCOL_INFO lpProtocolInfo = NULL;

    // variables needed for converting provider GUID to a string
    int iRet = 0;
    WCHAR GuidString[40] = { 0 };

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }

    lpProtocolInfo = (LPWSAPROTOCOL_INFO) MALLOC(dwBufferLen);
    if (lpProtocolInfo == NULL) {
        wprintf(L"Memory allocation for providers buffer failed\n");
        WSACleanup();
        return 1;
    }

    iNuminfo = WSAEnumProtocols(NULL, lpProtocolInfo, &dwBufferLen);
    if (iNuminfo == SOCKET_ERROR) {
        iError = WSAGetLastError();
        if (iError != WSAENOBUFS) {
            wprintf(L"WSAEnumProtocols failed with error: %d\n", iError);
            if (lpProtocolInfo) {
                FREE(lpProtocolInfo);
                lpProtocolInfo = NULL;
            }
            WSACleanup();
            return 1;
        } else {
            wprintf(L"WSAEnumProtocols failed with error: WSAENOBUFS (%d)\n",
                    iError);
            wprintf(L"  Increasing buffer size to %d\n\n", dwBufferLen);
            if (lpProtocolInfo) {
                FREE(lpProtocolInfo);
                lpProtocolInfo = NULL;
            }
            lpProtocolInfo = (LPWSAPROTOCOL_INFO) MALLOC(dwBufferLen);
            if (lpProtocolInfo == NULL) {
                wprintf(L"Memory allocation increase for buffer failed\n");
                WSACleanup();
                return 1;
            }
            iNuminfo = WSAEnumProtocols(NULL, lpProtocolInfo, &dwBufferLen);
            if (iNuminfo == SOCKET_ERROR) {
                iError = WSAGetLastError();
                wprintf(L"WSAEnumProtocols failed with error: %d\n", iError);
                if (lpProtocolInfo) {
                    FREE(lpProtocolInfo);
                    lpProtocolInfo = NULL;
                }
                WSACleanup();
                return 1;
            }

        }
    }

    wprintf(L"WSAEnumProtocols succeeded with protocol count = %d\n\n",
            iNuminfo);
    for (i = 0; i < iNuminfo; i++) {
        wprintf(L"Winsock Catalog Provider Entry #%d\n", i);
        wprintf
            (L"----------------------------------------------------------\n");
        wprintf(L"Entry type:\t\t\t ");
        if (lpProtocolInfo[i].ProtocolChain.ChainLen == 1)
            wprintf(L"Base Service Provider\n");
        else
            wprintf(L"Layered Chain Entry\n");

        wprintf(L"Protocol:\t\t\t %ws\n", lpProtocolInfo[i].szProtocol);

        iRet =
            StringFromGUID2(lpProtocolInfo[i].ProviderId,
                            (LPOLESTR) & GuidString, 39);
        if (iRet == 0)
            wprintf(L"StringFromGUID2 failed\n");
        else
            wprintf(L"Provider ID:\t\t\t %ws\n", GuidString);

        wprintf(L"Catalog Entry ID:\t\t %u\n",
                lpProtocolInfo[i].dwCatalogEntryId);

        wprintf(L"Version:\t\t\t %d\n", lpProtocolInfo[i].iVersion);

        wprintf(L"Address Family:\t\t\t %d\n",
                lpProtocolInfo[i].iAddressFamily);
        wprintf(L"Max Socket Address Length:\t %d\n",
                lpProtocolInfo[i].iMaxSockAddr);
        wprintf(L"Min Socket Address Length:\t %d\n",
                lpProtocolInfo[i].iMinSockAddr);

        wprintf(L"Socket Type:\t\t\t %d\n", lpProtocolInfo[i].iSocketType);
        wprintf(L"Socket Protocol:\t\t %d\n", lpProtocolInfo[i].iProtocol);
        wprintf(L"Socket Protocol Max Offset:\t %d\n",
                lpProtocolInfo[i].iProtocolMaxOffset);

        wprintf(L"Network Byte Order:\t\t %d\n",
                lpProtocolInfo[i].iNetworkByteOrder);
        wprintf(L"Security Scheme:\t\t %d\n",
                lpProtocolInfo[i].iSecurityScheme);
        wprintf(L"Max Message Size:\t\t %u\n", lpProtocolInfo[i].dwMessageSize);

        wprintf(L"ServiceFlags1:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags1);
        wprintf(L"ServiceFlags2:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags2);
        wprintf(L"ServiceFlags3:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags3);
        wprintf(L"ServiceFlags4:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags4);
        wprintf(L"ProviderFlags:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwProviderFlags);

        wprintf(L"Protocol Chain length:\t\t %d\n",
                lpProtocolInfo[i].ProtocolChain.ChainLen);

        wprintf(L"\n");
    }

    if (lpProtocolInfo) {
        FREE(lpProtocolInfo);
        lpProtocolInfo = NULL;
    }
    WSACleanup();

    return 0;
}


```






> [!NOTE]
> The winsock2.h header defines WSAEnumProtocols as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
