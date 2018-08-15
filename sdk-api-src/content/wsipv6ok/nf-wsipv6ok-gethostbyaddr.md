---
UID: NF:wsipv6ok.gethostbyaddr
title: gethostbyaddr macro
author: windows-sdk-content
description: gethostbyaddr is no longer recommended for use as of Windows Sockets 2.
old-location: winsock\gethostbyaddr_2.htm
old-project: winsock
ms.assetid: 303023e1-a486-4457-80f6-8aa80f6b2c79
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AF_INET, AF_INET6, AF_NETBIOS, _win32_gethostbyaddr_2, gethostbyaddr, gethostbyaddr function [Winsock], winsock.gethostbyaddr_2, wsipv6ok/gethostbyaddr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: wsipv6ok.h
req.include-header: Winsock2.h, Winsock.h
req.redist: 
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
tech.root: 
req.typenames: WSDXML_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - gethostbyaddr
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# gethostbyaddr macro


## -description


<p class="CCE_Message">[<b>gethostbyaddr</b> is no longer recommended for use as of Windows Sockets 2. Instead, use <a href="https://msdn.microsoft.com/7d1fb0ed-cc32-4b38-8ff5-88c2cca4f375">getnameinfo</a>.]

The 
<b>gethostbyaddr</b> function retrieves the host information corresponding to a network address.


## -parameters




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
 


## -remarks



The 
<b>gethostbyaddr</b> function returns a pointer to the 
<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure that contains the name and address corresponding to the given network address.

The memory for the <a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure  returned by the <b>gethostbyaddr</b> function is allocated internally by the Winsock DLL from thread local storage. Only a single <b>hostent</b> structure is allocated and used, no matter how many times the <b>gethostbyaddr</b> or <a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a> functions are called on the thread. The returned  <b>hostent</b> structure  must be copied to an application buffer if additional calls are to be made to the <b>gethostbyaddr</b> or <b>gethostbyname</b> functions on the same thread. Otherwise, the return value will be overwritten by subsequent <b>gethostbyaddr</b> or <b>gethostbyname</b> calls on the same thread. The internal memory allocated for the returned  <b>hostent</b> structure is released by the Winsock DLL when the thread exits. 

An application should not try to release the memory used by the returned <a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other function calls to <b>gethostbyaddr</b> or <a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a>.

Although 
<b>gethostbyaddr</b> no longer recommended for use as of Windows Sockets 2 and the <a href="https://msdn.microsoft.com/7d1fb0ed-cc32-4b38-8ff5-88c2cca4f375">getnameinfo</a> function should be used, 
<b>gethostbyaddr</b> is capable of returning a NetBIOS name; 
<b>getnameinfo</b> is not. Developers requiring NetBIOS name resolution may need to use <b>gethostbyaddr</b> until their applications are completely independent of NetBIOS names.


<div class="alert"><b>Note</b>   The capability to perform reverse lookups using the <b>gethostbyaddr</b> function is convenient, but such lookups are considered inherently unreliable, and should be used only as a hint.</div>
<div> </div>


<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>gethostbyaddr</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;stdio.h&gt;

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
    if (argc &lt; 2) {
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
    iResult = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    host_addr = argv[2];

    printf("Calling gethostbyaddr with %s\n", host_addr);
    if (bIpv6 == 1) {
        {
            iResult = inet_pton(AF_INET6, host_addr, &amp;addr6);
            if (iResult == 0) {
                printf("The IPv6 address entered must be a legal address\n");
                return 1;
            } else
                remoteHost = gethostbyaddr((char *) &amp;addr6, 16, AF_INET6);
        }
    } else {
        addr.s_addr = inet_addr(host_addr);
        if (addr.s_addr == INADDR_NONE) {
            printf("The IPv4 address entered must be a legal address\n");
            return 1;
        } else
            remoteHost = gethostbyaddr((char *) &amp;addr, 4, AF_INET);
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
        printf("\tOfficial name: %s\n", remoteHost-&gt;h_name);
        for (pAlias = remoteHost-&gt;h_aliases; *pAlias != 0; pAlias++) {
            printf("\tAlternate name #%d: %s\n", ++i, *pAlias);
        }
        printf("\tAddress type: ");
        switch (remoteHost-&gt;h_addrtype) {
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
            printf(" %d\n", remoteHost-&gt;h_addrtype);
            break;
        }
        printf("\tAddress length: %d\n", remoteHost-&gt;h_length);

        if (remoteHost-&gt;h_addrtype == AF_INET) {
            while (remoteHost-&gt;h_addr_list[i] != 0) {
                addr.s_addr = *(u_long *) remoteHost-&gt;h_addr_list[i++];
                printf("\tIPv4 Address #%d: %s\n", i, inet_ntoa(addr));
            }
        } else if (remoteHost-&gt;h_addrtype == AF_INET6)
            printf("\tRemotehost is an IPv6 address\n");
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/82436a88-5b37-4758-a5c9-b60dd1cbc36c">GetAddrInfoW</a>



<a href="https://msdn.microsoft.com/814cbb2e-8dd2-44b0-b8be-cfc5491bdc49">WSAAsyncGetHostByAddr</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a>



<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>



<a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>



<a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a>



<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a>
 

 

