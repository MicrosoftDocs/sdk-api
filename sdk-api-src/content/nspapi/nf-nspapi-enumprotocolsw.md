---
UID: NF:nspapi.EnumProtocolsW
title: EnumProtocolsW function (nspapi.h)
description: The EnumProtocols function retrieves information about a specified set of network protocols that are active on a local host. (Unicode)
helpviewer_keywords: ["EnumProtocols", "EnumProtocols function [Winsock]", "EnumProtocolsW", "IPPROTO_TCP", "IPPROTO_UDP", "ISOPROTO_TP4", "NSPROTO_IPX", "NSPROTO_SPX", "NSPROTO_SPXII", "_win32_enumprotocols_2", "nspapi/EnumProtocols", "nspapi/EnumProtocolsW", "winsock.enumprotocols_2"]
old-location: winsock\enumprotocols_2.htm
tech.root: WinSock
ms.assetid: 0310b80d-5036-46c2-b60f-1a6661cb7f94
ms.date: 12/05/2018
ms.keywords: EnumProtocols, EnumProtocols function [Winsock], EnumProtocolsA, EnumProtocolsW, IPPROTO_TCP, IPPROTO_UDP, ISOPROTO_TP4, NSPROTO_IPX, NSPROTO_SPX, NSPROTO_SPXII, _win32_enumprotocols_2, nspapi/EnumProtocols, nspapi/EnumProtocolsA, nspapi/EnumProtocolsW, winsock.enumprotocols_2
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumProtocolsW (Unicode) and EnumProtocolsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumProtocolsW
 - nspapi/EnumProtocolsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - EnumProtocols
 - EnumProtocolsA
 - EnumProtocolsW
---

# EnumProtocolsW function


## -description

The 
<b>EnumProtocols</b> function retrieves information about a specified set of network protocols that are active on a local host.


<div class="alert"><b>Note</b>  The 
<b>EnumProtocols</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, the reference material is included. The 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> function provides equivalent functionality in Windows Sockets 2.</div>
<div> </div>

## -parameters

### -param lpiProtocols [in, optional]

A pointer to a <b>null</b>-terminated array of protocol identifiers. The 
<b>EnumProtocols</b> function retrieves information about the protocols specified by this array. 




If <i>lpiProtocols</i> is <b>NULL</b>, the function retrieves information about all available protocols.

The following protocol identifier values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_TCP"></a><a id="ipproto_tcp"></a><dl>
<dt><b>IPPROTO_TCP</b></dt>
</dl>
</td>
<td width="60%">
The Transmission Control Protocol (TCP), a connection-oriented stream protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_UDP"></a><a id="ipproto_udp"></a><dl>
<dt><b>IPPROTO_UDP</b></dt>
</dl>
</td>
<td width="60%">
The User Datagram Protocol (UDP), a connectionless datagram protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="ISOPROTO_TP4"></a><a id="isoproto_tp4"></a><dl>
<dt><b>ISOPROTO_TP4</b></dt>
</dl>
</td>
<td width="60%">
The ISO connection-oriented transport protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="NSPROTO_IPX"></a><a id="nsproto_ipx"></a><dl>
<dt><b>NSPROTO_IPX</b></dt>
</dl>
</td>
<td width="60%">
The Internet Packet Exchange (IPX) protocol, a connectionless datagram protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="NSPROTO_SPX"></a><a id="nsproto_spx"></a><dl>
<dt><b>NSPROTO_SPX</b></dt>
</dl>
</td>
<td width="60%">
The Sequenced Packet Exchange (SPX) protocol, a connection-oriented stream protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="NSPROTO_SPXII"></a><a id="nsproto_spxii"></a><dl>
<dt><b>NSPROTO_SPXII</b></dt>
</dl>
</td>
<td width="60%">
The Sequenced Packet Exchange (SPX) protocol version 2, a connection-oriented stream protocol.

</td>
</tr>
</table>

### -param lpProtocolBuffer [out]

A pointer to a buffer that the function fills with an array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-protocol_infoa">PROTOCOL_INFO</a> data structures.

### -param lpdwBufferLength [in, out]

A pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by <i>lpProtocolBuffer</i>. 




On output, the function sets this variable to the minimum buffer size needed to retrieve all of the requested information. For the function to succeed, the buffer must be at least this size.

## -returns

If the function succeeds, the return value is the number of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-protocol_infoa">PROTOCOL_INFO</a> data structures written to the buffer pointed to by <i>lpProtocolBuffer</i>.

If the function fails, the return value is SOCKET_ERROR(–1). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns the following extended error code.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpProtocolBuffer</i> was too small to receive all of the relevant 
<a href="/windows/desktop/api/nspapi/ns-nspapi-protocol_infoa">PROTOCOL_INFO</a> structures. Call the function with a buffer at least as large as the value returned in *<i>lpdwBufferLength</i>.

</td>
</tr>
</table>

## -remarks

In the following sample code, the 
<b>EnumProtocols</b> function retrieves information about all protocols that are available on a system. The code then examines each of the protocols in greater detail.


```cpp
#define WIN32_LEAN_AND_MEAN

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <Nspapi.h>
#include <stdlib.h>
#include <stdio.h>


// Need to link with Ws2_32.lib and Mswsock.lib
#pragma comment (lib, "Ws2_32.lib")
#pragma comment (lib, "Mswsock.lib")

int FindProtocol(BOOL Reliable, 
    BOOL MessageOriented, BOOL StreamOriented, 
    BOOL Connectionless, DWORD *ProtocolUsed); 

int __cdecl main(int argc, char **argv)
{
    WSADATA wsaData;

    int ProtocolError = SOCKET_ERROR;
    int iResult;
    
    BOOLEAN bReliable = FALSE;
    BOOLEAN bMessageOriented = FALSE;
    BOOLEAN bStreamOriented = TRUE;
    BOOLEAN bConnectionless = FALSE;
    DWORD *pProtocols = NULL;
    
    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s servicename\n", argv[0]);
        return 1;
    }

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    
    ProtocolError = FindProtocol( bReliable, bMessageOriented,
        bStreamOriented, bConnectionless, pProtocols);
    if (ProtocolError == SOCKET_ERROR) {
        printf("Unable to find a protocol to support the parameters requested\n");
        return 1;
    }
    
    // Connect to the servicename ...    
    
    return 0;

}

#define MAX_PROTOCOLS 1024

int FindProtocol ( 
    BOOL Reliable, 
    BOOL MessageOriented, 
    BOOL StreamOriented, 
    BOOL Connectionless, 
    DWORD *ProtocolUsed 
    ) 
{ 
    // local variables 
    INT protocols[MAX_PROTOCOLS+1]; 
    BYTE buffer[2048]; 
    DWORD bytesRequired; 
    INT err; 
    PPROTOCOL_INFO protocolInfo; 
    INT protocolCount; 
    INT i; 
    DWORD protocolIndex; 
//    PCSADDR_INFO csaddrInfo; 
//    INT addressCount; 
//    SOCKET s; 
 
    // First look up the protocols installed on this computer. 
    // 
    bytesRequired = sizeof(buffer); 
    err = EnumProtocols( NULL, buffer, &bytesRequired ); 
    if ( err <= 0 ) 
        return SOCKET_ERROR; 
 
    // Walk through the available protocols and pick out the ones which 
    // support the desired characteristics. 
    // 
    protocolCount = err; 
    protocolInfo = (PPROTOCOL_INFO)buffer; 
 
    for ( i = 0, protocolIndex = 0; 
        i < protocolCount && protocolIndex < MAX_PROTOCOLS; 
        i++, protocolInfo++ ) { 
 
        // If connection-oriented support is requested, then check if 
        // supported by this protocol.  We assume here that connection- 
        // oriented support implies fully reliable service. 
        // 
 
        if ( Reliable ) { 
            // Check to see if the protocol is reliable.  It must 
            // guarantee both delivery of all data and the order in 
            // which the data arrives. 
            // 
            if ( (protocolInfo->dwServiceFlags & 
                    XP_GUARANTEED_DELIVERY) == 0 
                || 
                    (protocolInfo->dwServiceFlags & 
                    XP_GUARANTEED_ORDER) == 0 ) { 
 
                continue; 
            } 
 
            // Check to see that the protocol matches the stream/message 
            // characteristics requested. 
            // 
            if ( StreamOriented && 
                (protocolInfo->dwServiceFlags & XP_MESSAGE_ORIENTED) 
                    != 0 && 
                (protocolInfo->dwServiceFlags & XP_PSEUDO_STREAM) 
                     == 0 ) { 
                continue; 
            } 
 
            if ( MessageOriented && 
                    (protocolInfo->dwServiceFlags & XP_MESSAGE_ORIENTED) 
                              == 0 ) { 
                continue; 
            } 
 
        } 
        else if ( Connectionless ) { 
            // Make sure that this is a connectionless protocol. 
            // 
            if ( (protocolInfo->dwServiceFlags & XP_CONNECTIONLESS) 
                     != 0 ) 
                continue; 
        } 
 
        // This protocol fits all the criteria.  Add it to the list of 
        // protocols in which we're interested. 
        // 
        protocols[protocolIndex++] = protocolInfo->iProtocol; 
     }

     *ProtocolUsed = (INT) protocolIndex;
     return 0;
}

```






> [!NOTE]
> The nspapi.h header defines EnumProtocols as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/nspapi/nf-nspapi-getaddressbynamea">GetAddressByName</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-protocol_infoa">PROTOCOL_INFO</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
