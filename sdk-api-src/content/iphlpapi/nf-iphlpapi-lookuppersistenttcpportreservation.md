---
UID: NF:iphlpapi.LookupPersistentTcpPortReservation
title: LookupPersistentTcpPortReservation function (iphlpapi.h)
description: Looks up the token for a persistent TCP port reservation for a consecutive block of TCP ports on the local computer.
helpviewer_keywords: ["LookupPersistentTcpPortReservation","LookupPersistentTcpPortReservation function [IP Helper]","iphlp.lookuppersistenttcpportreservation","iphlpapi/LookupPersistentTcpPortReservation"]
old-location: iphlp\lookuppersistenttcpportreservation.htm
tech.root: IpHlp
ms.assetid: 5EBEB774-13A2-49C2-92ED-5271081615AA
ms.date: 12/05/2018
ms.keywords: LookupPersistentTcpPortReservation, LookupPersistentTcpPortReservation function [IP Helper], iphlp.lookuppersistenttcpportreservation, iphlpapi/LookupPersistentTcpPortReservation
req.header: iphlpapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LookupPersistentTcpPortReservation
 - iphlpapi/LookupPersistentTcpPortReservation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - LookupPersistentTcpPortReservation
---

# LookupPersistentTcpPortReservation function


## -description

The 
<b>LookupPersistentTcpPortReservation</b> function looks up the token for a persistent TCP port reservation for a consecutive block of TCP ports on the local computer.

## -parameters

### -param StartPort [in]

The starting TCP port number in network byte order.

### -param NumberOfPorts [in]

The number of TCP port numbers  that were reserved.

### -param Token [out]

A pointer to a port reservation token that is returned if the function succeeds.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if zero is passed in the <i>StartPort</i>  or <i>NumberOfPorts</i> parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The element was not found. This error is returned if persistent port block specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters could not be found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>LookupPersistentTcpPortReservation</b>  function is defined on Windows Vista and later. 

The <b>LookupPersistentTcpPortReservation</b>  function is used to lookup the token for a persistent reservation for a block of TCP ports. 

A persistent reservation for a block of TCP ports is  created by a call to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a> function. The <i>StartPort</i>  or <i>NumberOfPorts</i> parameters passed to the <b>LookupPersistentTcpPortReservation</b>  function must match the values used when the persistent reservation for a block of TCP ports was created by  the <b>CreatePersistentTcpPortReservation</b> function.

If the <b>LookupPersistentTcpPortReservation</b> function succeeds, the <i>Token</i> parameter returned will point to the token for the persistent port reservation for the block of TCP ports. Note that the token for a given persistent reservation for a block of TCP ports may change each time the system is restarted.



An application can request port assignments from the TCP port reservation by opening a TCP socket, then calling the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function specifying the <a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a> IOCTL and passing the reservation token before issuing a call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function on the socket. 


#### Examples

The following example looks up a persistent TCP port reservation and then creates a socket and allocates a port from the port reservation. 


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with iphlpapi.lib
#pragma comment(lib, "iphlpapi.lib")

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR **argv)  {

    // Declare and initialize variables
    
    int startPort = 0;         // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;    // Network byte order
    ULONG64 resToken = {0};
    
    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = SOCK_STREAM;
    int iProtocol = IPPROTO_TCP;

    DWORD bytesReturned = 0;

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service; 
    sockaddr_in sockName;
    int nameLen = sizeof(sockName);
    
    // Validate the parameters
    if (argc != 3) {
        wprintf(L"usage: %s <Starting Port> <Number of Ports>\n", 
            argv[0]);
        wprintf(L"Look up a persistent TCP port reservation\n");
        wprintf(L"Example usage:\n");
        wprintf(L"   %s 5000 20\n", argv[0]);
        wprintf(L"   where StartPort=5000 NumPorts=20");
        return 1;
    }

    startPort = _wtoi(argv[1]);
    if ( startPort < 0 || startPort> 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }    
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[2]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }    

    status = LookupPersistentTcpPortReservation((USHORT) startPortns, (USHORT) numPorts, &resToken);
    if( status != NO_ERROR )
    {
        wprintf(L"LookupPersistentTcpPortReservation returned error: %ld\n", 
            status);
        return 1;
    }

    wprintf(L"LookupPersistentTcpPortReservation call succeeded\n");
    wprintf(L"  Token = %I64d\n", resToken);  
  
    // Comment out this block if you don't want to create a socket and associate it with the 
    // persistent reservation

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET)
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
    else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION, (LPVOID) & resToken,
                     sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf
                (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                 WSAGetLastError());
        } else {
            wprintf(L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n", 
                bytesReturned);                

            service.sin_family = AF_INET;
            service.sin_addr.s_addr = INADDR_ANY;
            service.sin_port = 0;

            iResult = bind(sock, (SOCKADDR*) &service, sizeof(service) );
            if (iResult == SOCKET_ERROR)
                wprintf(L"bind failed with error = %d\n", WSAGetLastError());
            else {
                wprintf(L"bind succeeded\n");
                iResult = getsockname(sock, (SOCKADDR*) &sockName, &nameLen);
                if (iResult == SOCKET_ERROR) 
                    wprintf(L"getsockname failed with error = %d\n", WSAGetLastError() );
                else {
                    wprintf(L"getsockname succeeded\n");
                    wprintf(L"Port number allocated = %u\n", ntohs(sockName.sin_port) );
                }
            }                  
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket failed with error = %d\n", WSAGetLastError());
            }
        }
    }
    WSACleanup();

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a>



<a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a>