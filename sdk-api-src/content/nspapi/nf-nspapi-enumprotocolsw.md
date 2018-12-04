---
UID: NF:nspapi.EnumProtocolsW
title: EnumProtocolsW function
author: windows-sdk-content
description: The EnumProtocols function retrieves information about a specified set of network protocols that are active on a local host.
old-location: winsock\enumprotocols_2.htm
tech.root: winsock
ms.assetid: 0310b80d-5036-46c2-b60f-1a6661cb7f94
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: EnumProtocols, EnumProtocols function [Winsock], EnumProtocolsA, EnumProtocolsW, IPPROTO_TCP, IPPROTO_UDP, ISOPROTO_TP4, NSPROTO_IPX, NSPROTO_SPX, NSPROTO_SPXII, _win32_enumprotocols_2, nspapi/EnumProtocols, nspapi/EnumProtocolsA, nspapi/EnumProtocolsW, winsock.enumprotocols_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumProtocolsW function


## -description


The 
<b>EnumProtocols</b> function retrieves information about a specified set of network protocols that are active on a local host.


<div class="alert"><b>Note</b>  The 
<b>EnumProtocols</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, the reference material is included. The 
<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a> function provides equivalent functionality in Windows Sockets 2.</div>
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
<a href="https://msdn.microsoft.com/0cbddf17-41a8-4e61-b3b0-080ef50dc5de">PROTOCOL_INFO</a> data structures.


### -param lpdwBufferLength [in, out]

A pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by <i>lpProtocolBuffer</i>. 




On output, the function sets this variable to the minimum buffer size needed to retrieve all of the requested information. For the function to succeed, the buffer must be at least this size.


## -returns



If the function succeeds, the return value is the number of 
<a href="https://msdn.microsoft.com/0cbddf17-41a8-4e61-b3b0-080ef50dc5de">PROTOCOL_INFO</a> data structures written to the buffer pointed to by <i>lpProtocolBuffer</i>.

If the function fails, the return value is SOCKET_ERROR(–1). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which returns the following extended error code.

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
<a href="https://msdn.microsoft.com/0cbddf17-41a8-4e61-b3b0-080ef50dc5de">PROTOCOL_INFO</a> structures. Call the function with a buffer at least as large as the value returned in *<i>lpdwBufferLength</i>.

</td>
</tr>
</table>
 




## -remarks



In the following sample code, the 
<b>EnumProtocols</b> function retrieves information about all protocols that are available on a system. The code then examines each of the protocols in greater detail.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define WIN32_LEAN_AND_MEAN

#include &lt;windows.h&gt;
#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;Nspapi.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;stdio.h&gt;


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
    iResult = WSAStartup(MAKEWORD(2,2), &amp;wsaData);
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
    err = EnumProtocols( NULL, buffer, &amp;bytesRequired ); 
    if ( err &lt;= 0 ) 
        return SOCKET_ERROR; 
 
    // Walk through the available protocols and pick out the ones which 
    // support the desired characteristics. 
    // 
    protocolCount = err; 
    protocolInfo = (PPROTOCOL_INFO)buffer; 
 
    for ( i = 0, protocolIndex = 0; 
        i &lt; protocolCount &amp;&amp; protocolIndex &lt; MAX_PROTOCOLS; 
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
            if ( (protocolInfo-&gt;dwServiceFlags &amp; 
                    XP_GUARANTEED_DELIVERY) == 0 
                || 
                    (protocolInfo-&gt;dwServiceFlags &amp; 
                    XP_GUARANTEED_ORDER) == 0 ) { 
 
                continue; 
            } 
 
            // Check to see that the protocol matches the stream/message 
            // characteristics requested. 
            // 
            if ( StreamOriented &amp;&amp; 
                (protocolInfo-&gt;dwServiceFlags &amp; XP_MESSAGE_ORIENTED) 
                    != 0 &amp;&amp; 
                (protocolInfo-&gt;dwServiceFlags &amp; XP_PSEUDO_STREAM) 
                     == 0 ) { 
                continue; 
            } 
 
            if ( MessageOriented &amp;&amp; 
                    (protocolInfo-&gt;dwServiceFlags &amp; XP_MESSAGE_ORIENTED) 
                              == 0 ) { 
                continue; 
            } 
 
        } 
        else if ( Connectionless ) { 
            // Make sure that this is a connectionless protocol. 
            // 
            if ( (protocolInfo-&gt;dwServiceFlags &amp; XP_CONNECTIONLESS) 
                     != 0 ) 
                continue; 
        } 
 
        // This protocol fits all the criteria.  Add it to the list of 
        // protocols in which we're interested. 
        // 
        protocols[protocolIndex++] = protocolInfo-&gt;iProtocol; 
     }

     *ProtocolUsed = (INT) protocolIndex;
     return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ea257b9e-5c5b-41fb-bcf0-7ac10b563b8c">GetAddressByName</a>



<a href="https://msdn.microsoft.com/0cbddf17-41a8-4e61-b3b0-080ef50dc5de">PROTOCOL_INFO</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

