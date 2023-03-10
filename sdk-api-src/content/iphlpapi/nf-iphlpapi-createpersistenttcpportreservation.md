---
UID: NF:iphlpapi.CreatePersistentTcpPortReservation
title: CreatePersistentTcpPortReservation function (iphlpapi.h)
description: Creates a persistent TCP port reservation for a consecutive block of TCP ports on the local computer.
helpviewer_keywords: ["CreatePersistentTcpPortReservation","CreatePersistentTcpPortReservation function [IP Helper]","iphlp.createpersistenttcpportreservation","iphlpapi/CreatePersistentTcpPortReservation"]
old-location: iphlp\createpersistenttcpportreservation.htm
tech.root: IpHlp
ms.assetid: 19DAF828-B0E4-49E2-843D-7350C8083C45
ms.date: 12/05/2018
ms.keywords: CreatePersistentTcpPortReservation, CreatePersistentTcpPortReservation function [IP Helper], iphlp.createpersistenttcpportreservation, iphlpapi/CreatePersistentTcpPortReservation
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
 - CreatePersistentTcpPortReservation
 - iphlpapi/CreatePersistentTcpPortReservation
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
 - CreatePersistentTcpPortReservation
---

# CreatePersistentTcpPortReservation function


## -description

The 
<b>CreatePersistentTcpPortReservation</b> function creates a persistent TCP port reservation for a consecutive block of TCP ports on the local computer.

## -parameters

### -param StartPort [in]

The starting TCP port number in network byte order.

### -param NumberOfPorts [in]

The number of TCP port numbers to reserve.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. 

This error is returned if zero is passed in the <i>StartPort</i>  or <i>NumberOfPorts</i> parameters. This error is also returned if the <i>NumberOfPorts</i> parameter is too large a block of ports depending on the <i>StartPort</i> parameter that the allocable block of ports would exceed the maximum port that can be allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHARING_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
The process cannot access the file because it is being used by another process. This error is returned if a TCP port in the block of TCP ports specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters is already being used. This error is also returned if a persistent reservation for a block of TCP ports specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters matches or overlaps a persistent reservation for a block of TCP ports that was already created. 

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

The <b>CreatePersistentTcpPortReservation</b> function is defined on Windows Vista and later. 

The <b>CreatePersistentTcpPortReservation</b> function is used to add a persistent reservation for a block of TCP ports. 

Applications and services which need to reserve ports fall into two categories. The first category includes components which need a particular port as part of their operation. Such components will generally prefer to specify their required port at installation time (in an application manifest, for example). The second category includes components which need any available port or block of ports at runtime. 

These two categories correspond to specific and wildcard port reservation requests. Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime. 

The <b>CreatePersistentTcpPortReservation</b> function provides the ability for an application or service to reserve a persistent block of TCP ports.  Persistent TCP port reservations are recorded in a persistent store for the TCP module in Windows. 

A caller obtains a persistent port reservation by specifying how many ports are required and whether a specific range is needed. If the request can be satisfied, the <b>CreatePersistentTcpPortReservation</b> function returns a unique opaque ULONG64 token, which subsequently identifies the reservation. A persistent TCP port reservation may be released by calling the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a> function. Note that the token for a given persistent TCP port reservation may change each time the system is restarted.



Windows does not implement inter-component security for persistent reservations obtained using these functions. This means that if a component is granted the ability to obtain any persistent port reservations, that component automatically gains the ability to consume any persistent port reservations granted to any other component on the system. Process-level security is enforced for runtime reservations, but such control cannot be extended to persistent port reservations created using the <b>CreatePersistentTcpPortReservation</b> or  <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a> function.



Once a persistent TCP port reservation has been obtained, an application can request port assignments from the TCP port reservation by opening a TCP socket, then calling the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function specifying the <a href="/windows/win32/winsock/sio-associate-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a> IOCTL and passing the reservation token before issuing a call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function on the socket. 

The <a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a> IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports. For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted. Runtime port reservations last only as long as the lifetime of the socket on which the <b>SIO_ACQUIRE_PORT_RESERVATION</b> IOCTL was called.  In contrast, persistent port reservations created using the <b>CreatePersistentTcpPortReservation</b> function may be consumed by any process with the ability to obtain persistent reservations. 



The <b>CreatePersistentTcpPortReservation</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreatePersistentTcpPortReservation</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.




#### Examples

The following example creates a persistent TCP port reservation, then creates a socket and allocates a port from the port reservation, and then closes the socket and deletes the TCP port reservation. 

This example must be run by a user that is a member of the Administrators group. The simplest way to run this example is in an enhanced shell as the built-in Administrator (RunAs administrator). 


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

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;         // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;    // Network byte order
    ULONG64 resToken = { 0 };

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
        wprintf(L"Creates a persistent TCP port reservation\n");
        wprintf(L"Example usage:\n");
        wprintf(L"   %s 5000 20\n", argv[0]);
        wprintf(L"   where StartPort=5000 NumPorts=20");
        return 1;
    }

    startPort = _wtoi(argv[1]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[2]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    status =
        CreatePersistentTcpPortReservation((USHORT) startPortns, (USHORT) numPorts,
                                           &resToken);
    if (status != NO_ERROR) {
        wprintf(L"CreatePersistentTcpPortReservation returned error: %ld\n", status);
        return 1;
    }

    wprintf(L"CreatePersistentTcpPortReservation call succeeded\n");
    wprintf(L"  Token = %I64d\n", resToken);

    // Comment out this block if you don't want to create a socket and associate it with the 
    // persistent reservation

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        // return 1;
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
                WSACleanup();
            }
        }
    }

    // comment out this block of code if you don't want to delete the reservation just created
    status = DeletePersistentTcpPortReservation((USHORT) startPortns, (USHORT) numPorts);
    if (status != NO_ERROR) {
        wprintf(L"DeletePersistentTcpPortReservation returned error: %ld\n", status);
        return 1;
    }
    wprintf(L"DeletePersistentTcpPortReservation call succeeded\n");

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a>



<a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ACQUIRE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-acquire-port-reservation">SIO_ASSOCIATE_PORT_RESERVATION</a>



<a href="/windows/win32/winsock/sio-release-port-reservation">SIO_RELEASE_PORT_RESERVATION</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>