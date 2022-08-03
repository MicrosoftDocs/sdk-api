---
UID: NF:winsock2.gethostbyaddr
title: gethostbyaddr function (winsock2.h)
description: The gethostbyaddr function  retrieves the host information corresponding to a network address. (gethostbyaddr is no longer recommended, use getnameinfo instead)
helpviewer_keywords: ["AF_INET","AF_INET6","AF_NETBIOS","_win32_gethostbyaddr_2","gethostbyaddr","gethostbyaddr function [Winsock]","winsock.gethostbyaddr_2","wsipv6ok/gethostbyaddr"]
old-location: winsock\gethostbyaddr_2.htm
tech.root: WinSock
ms.assetid: 303023e1-a486-4457-80f6-8aa80f6b2c79
ms.date: 08/03/2022
ms.keywords: AF_INET, AF_INET6, AF_NETBIOS, _win32_gethostbyaddr_2, gethostbyaddr, gethostbyaddr function [Winsock], winsock.gethostbyaddr_2, wsipv6ok/gethostbyaddr
req.header: winsock2.h
req.include-header: Winsock2.h, Winsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - gethostbyaddr
 - winsock2/gethostbyaddr
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
 - gethostbyaddr
---

# gethostbyaddr function


## -description

<p class="CCE_Message">[<b>gethostbyaddr</b> is no longer recommended for use as of Windows Sockets 2. Instead, use <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a>.]

The 
<b>gethostbyaddr</b> function retrieves the host information corresponding to a network address.

## -parameters

### -param addr

TBD

### -param len

TBD

### -param type

TBD




#### - a [in]

A pointer to an address in network byte order.


#### - b [in]

The length, in bytes, of the address.


#### - c [in]

The type of the address, such as the AF_INET address family type (used with TCP, UDP, and other associated Internet protocols). Possible values for the address family are defined in the Winsock2.h header file. 

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the possible values for the address family are defined in the Ws2def.h header file. Note that the Ws2def.h header file is automatically included in Winsock2.h, and should never be used directly.

Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

The table below lists the possible values for address family that are supported. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_NETBIOS"></a><a id="af_netbios"></a><dl>
<dt><b>AF_NETBIOS</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The NetBIOS address family. This address family is only supported if a Windows Sockets provider for NetBIOS is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family.

</td>
</tr>
</table>

## -returns

If no error occurs, 
<b>gethostbyaddr</b> returns a pointer to the 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure. Otherwise, it returns a null pointer, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was supplied. This error is returned if <b>AF_INET6</b> was specified in the  <i>type</i> parameter and the <i>len</i> parameter was not set equal to the size of an IPv6 address.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative answer host not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
Nonauthoritative host not found, or server failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
Valid name, no data record of requested type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>type</i> specified is not supported by the Windows Sockets implementation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>addr</i> parameter is not a valid part of the user address space, or the <i>len</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Socket 1.1 call was canceled through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.

</td>
</tr>
</table>

## -remarks

The 
<b>gethostbyaddr</b> function returns a pointer to the 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure that contains the name and address corresponding to the given network address.

The memory for the <a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure  returned by the <b>gethostbyaddr</b> function is allocated internally by the Winsock DLL from thread local storage. Only a single <b>hostent</b> structure is allocated and used, no matter how many times the <b>gethostbyaddr</b> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a> functions are called on the thread. The returned  <b>hostent</b> structure  must be copied to an application buffer if additional calls are to be made to the <b>gethostbyaddr</b> or <b>gethostbyname</b> functions on the same thread. Otherwise, the return value will be overwritten by subsequent <b>gethostbyaddr</b> or <b>gethostbyname</b> calls on the same thread. The internal memory allocated for the returned  <b>hostent</b> structure is released by the Winsock DLL when the thread exits. 

An application should not try to release the memory used by the returned <a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other function calls to <b>gethostbyaddr</b> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a>.

Although 
<b>gethostbyaddr</b> no longer recommended for use as of Windows Sockets 2 and the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a> function should be used, 
<b>gethostbyaddr</b> is capable of returning a NetBIOS name; 
<b>getnameinfo</b> is not. Developers requiring NetBIOS name resolution may need to use <b>gethostbyaddr</b> until their applications are completely independent of NetBIOS names.


<div class="alert"><b>Note</b>   The capability to perform reverse lookups using the <b>gethostbyaddr</b> function is convenient, but such lookups are considered inherently unreliable, and should be used only as a hint.</div>
<div> </div>


<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>gethostbyaddr</b> function.


```cpp
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

int main(int argc, char **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    DWORD dwError;
    int i = 0;
    int bIpv6 = 0;

    struct hostent *remoteHost;
    char *host_addr;
    struct in_addr addr = { 0 };
    IN6_ADDR addr6;

    char **pAlias;

    // Validate the parameters
    if (argc < 2) {
        printf("usage: %s 4 ipv4address\n", argv[0]);
        printf(" or\n");
        printf("usage: %s 6 ipv6address\n", argv[0]);
        printf("  to return the hostname\n");
        printf("       %s 4 127.0.0.1\n", argv[0]);
        printf("       %s 6 0::1\n", argv[0]);
        return 1;
    }
    // Validate parameters 
    if (atoi(argv[1]) == 4)
        bIpv6 = 0;
    else if (atoi(argv[1]) == 6)
        bIpv6 = 1;
    else {
        printf("usage: %s 4 ipv4address\n", argv[0]);
        printf(" or\n");
        printf("usage: %s 6 ipv6address\n", argv[0]);
        printf("  to return the hostname\n");
        printf("       %s 4 127.0.0.1\n", argv[0]);
        printf("       %s 6 0::1\n", argv[0]);
        return 1;
    }

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    host_addr = argv[2];

    printf("Calling gethostbyaddr with %s\n", host_addr);
    if (bIpv6 == 1) {
        {
            iResult = inet_pton(AF_INET6, host_addr, &addr6);
            if (iResult == 0) {
                printf("The IPv6 address entered must be a legal address\n");
                return 1;
            } else
                remoteHost = gethostbyaddr((char *) &addr6, 16, AF_INET6);
        }
    } else {
        addr.s_addr = inet_addr(host_addr);
        if (addr.s_addr == INADDR_NONE) {
            printf("The IPv4 address entered must be a legal address\n");
            return 1;
        } else
            remoteHost = gethostbyaddr((char *) &addr, 4, AF_INET);
    }

    if (remoteHost == NULL) {
        dwError = WSAGetLastError();
        if (dwError != 0) {
            if (dwError == WSAHOST_NOT_FOUND) {
                printf("Host not found\n");
                return 1;
            } else if (dwError == WSANO_DATA) {
                printf("No data record found\n");
                return 1;
            } else {
                printf("Function failed with error: %ld\n", dwError);
                return 1;
            }
        }
    } else {
        printf("Function returned:\n");
        printf("\tOfficial name: %s\n", remoteHost->h_name);
        for (pAlias = remoteHost->h_aliases; *pAlias != 0; pAlias++) {
            printf("\tAlternate name #%d: %s\n", ++i, *pAlias);
        }
        printf("\tAddress type: ");
        switch (remoteHost->h_addrtype) {
        case AF_INET:
            printf("AF_INET\n");
            break;
        case AF_INET6:
            printf("AF_INET6\n");
            break;
        case AF_NETBIOS:
            printf("AF_NETBIOS\n");
            break;
        default:
            printf(" %d\n", remoteHost->h_addrtype);
            break;
        }
        printf("\tAddress length: %d\n", remoteHost->h_length);

        if (remoteHost->h_addrtype == AF_INET) {
            while (remoteHost->h_addr_list[i] != 0) {
                addr.s_addr = *(u_long *) remoteHost->h_addr_list[i++];
                printf("\tIPv4 Address #%d: %s\n", i, inet_ntoa(addr));
            }
        } else if (remoteHost->h_addrtype == AF_INET6)
            printf("\tRemotehost is an IPv6 address\n");
    }

    return 0;
}

```


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyaddr">WSAAsyncGetHostByAddr</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname">gethostbyname</a>



<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a>
