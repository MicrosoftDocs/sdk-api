---
UID: NF:winsock.gethostbyname
title: gethostbyname function (winsock.h)
description: The gethostbyname function (winsock.h) retrieves host information corresponding to a host name from a host database.
helpviewer_keywords: ["_win32_gethostbyname_2","gethostbyname","gethostbyname function [Winsock]","winsock.gethostbyname_2","wsipv6ok/gethostbyname"]
old-location: winsock\gethostbyname_2.htm
tech.root: WinSock
ms.assetid: 2526ecb5-927b-40c8-8d8f-919e7986ff05
ms.date: 08/15/2022
ms.keywords: _win32_gethostbyname_2, gethostbyname, gethostbyname function [Winsock], winsock.gethostbyname_2, wsipv6ok/gethostbyname
req.header: winsock.h
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
 - gethostbyname
 - winsock/gethostbyname
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
 - gethostbyname
---

# gethostbyname function


## -description

The 
<b>gethostbyname</b> function retrieves host information corresponding to a host name from a host database.


<div class="alert"><b>Note</b>  The 
<b>gethostbyname</b> function has been deprecated by the introduction of the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function. Developers creating Windows Sockets 2 applications are urged to use the 
<b>getaddrinfo</b> function instead of 
<b>gethostbyname</b>.</div>
<div> </div>

## -parameters

### -param name

TBD




#### - a [in]

A pointer to the <b>null</b>-terminated name of the host to resolve.

## -returns

If no error occurs, 
<b>gethostbyname</b> returns a pointer to the 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure described above. Otherwise, it returns a <b>null</b> pointer and a specific error number can be retrieved by calling 
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
Nonauthoritative host not found, or server failure.

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
The requested name is valid, but no data of the requested type was found. This error is also returned if the <i>name</i> parameter contains a string representation of an IPv6 address or an illegal IPv4 address. 

This error should not be interpreted to mean that the <i>name</i> parameter contains a name string that has been validated for a particular protocol (an IP hostname, for example). Since Winsock supports multiple name service providers, a name may potentially be valid for one provider and not accepted by another provider.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter is not a valid part of the user address space.

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
<b>gethostbyname</b> function returns a pointer to a 
<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure—a structure allocated by Windows Sockets. The 
<b>hostent</b> structure contains the results of a successful search for the host specified in the <i>name</i> parameter. 

If the host specified in the <i>name</i> parameter has both IPv4 and IPv6 addresses, only the IPv4 addresses will be returned. The  <b>gethostbyname</b> function can only return IPv4 addresses for the <i>name</i> parameter. The  <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function and associated <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure should be used if IPv6 addresses for the host are required or if both IPv4 and IPv6 addresses for the host are required.

If the <i>name</i> parameter points to an empty string or <i>name</i> is <b>NULL</b>, the returned string is the same as the string returned by a successful 
<a href="/windows/desktop/api/winsock/nf-winsock-gethostname">gethostname</a> function call (the standard host name for the local computer).

If the <i>name</i> parameter contains a string representation of a legal IPv4 address, then the binary IPv4 address that represents the string is returned in the <a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure. The <b>h_name</b> member of the <b>hostent</b> structure contains the string representation of the IPv4 address and the <b>h_addr_list</b>  contains the binary IPv4 address. If the <i>name</i> parameter contains a string representation of an IPv6 address or an illegal IPv4 address, then the  <b>gethostbyname</b> function will fail and return <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a>.  

The memory for the <a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure  returned by the <b>gethostbyname</b> function is allocated internally by the Winsock DLL from thread local storage. Only a single <b>hostent</b> structure is allocated and used, no matter how many times the <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr">gethostbyaddr</a> 
		 or <b>gethostbyname</b> functions are called on the thread. The returned  <b>hostent</b> structure  must be copied to an application buffer if additional calls are to be made to the <b>gethostbyname</b> or <b>gethostbyaddr</b> functions on the same thread. Otherwise, the return value will be overwritten by subsequent <b>gethostbyname</b> or <b>gethostbyaddr</b> 
		 calls on the same thread. The internal memory allocated for the returned  <b>hostent</b> structure is released by the Winsock DLL when the thread exits. 

An application should not try to release the memory used by the returned <a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a> structure. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other function calls to <b>gethostbyname</b> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr">gethostbyaddr</a> 
		.

The 
<b>gethostbyname</b> function cannot take an IP address string as a parameter passed to it in the <i>name</i> and resolve it to a host name. Such a request is treated exactly as a string representation of an IPv4 address or an unknown host name were passed. An application can use the <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a> to convert an IPv4 address string to a binary IPv4 address, then use another function, 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr">gethostbyaddr</a>, to resolve the IPv4 address to a host name.  


<div class="alert"><b>Note</b>  The <b>gethostbyname</b> function does not check the size of the <i>name</i> parameter before passing the buffer. With an improperly sized <i>name</i> parameter, heap corruption can occur.</div>
<div> </div>


<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following examples demonstrates the use of the <b>gethostbyname</b> function.


```cpp
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <windows.h>
#pragma comment(lib, "ws2_32.lib")

int main(int argc, char **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    DWORD dwError;
    int i = 0;

    struct hostent *remoteHost;
    char *host_name;
    struct in_addr addr;

    char **pAlias;

    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s hostname\n", argv[0]);
        printf("  to return the IP addresses for the host\n");
        printf("       %s www.contoso.com\n", argv[0]);
        printf(" or\n");
        printf("       %s IPv4string\n", argv[0]);
        printf("  to return an IPv4 binary address for an IPv4string\n");
        printf("       %s 127.0.0.1\n", argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    host_name = argv[1];

    printf("Calling gethostbyname with %s\n", host_name);
    remoteHost = gethostbyname(host_name);
    
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
        case AF_NETBIOS:
            printf("AF_NETBIOS\n");
            break;
        default:
            printf(" %d\n", remoteHost->h_addrtype);
            break;
        }
        printf("\tAddress length: %d\n", remoteHost->h_length);

        i = 0;
        if (remoteHost->h_addrtype == AF_INET)
        {
            while (remoteHost->h_addr_list[i] != 0) {
                addr.s_addr = *(u_long *) remoteHost->h_addr_list[i++];
                printf("\tIP Address #%d: %s\n", i, inet_ntoa(addr));
            }
        }
        else if (remoteHost->h_addrtype == AF_NETBIOS)
        {   
            printf("NETBIOS address was returned\n");
        }   
    }

    return 0;
}

```


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname">WSAAsyncGetHostByName</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr">gethostbyaddr</a>



<a href="/windows/desktop/api/winsock/nf-winsock-gethostname">gethostname</a>



<a href="/windows/desktop/api/winsock/ns-winsock-hostent">hostent</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>
