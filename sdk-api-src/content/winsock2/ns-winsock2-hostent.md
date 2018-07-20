---
UID: NS:winsock2.hostent
title: hostent
author: windows-sdk-content
description: The hostent structure is used by functions to store information about a given host, such as host name, IPv4 address, and so forth.
old-location: winsock\hostent_2.htm
old-project: winsock
ms.assetid: f194b9d5-dfaf-4a02-95c6-6d06015aad1d
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPHOSTENT, *PHOSTENT, FAR *LPHOSTENT, FAR *LPHOSTENT structure [Winsock], HOSTENT, HOSTENT structure [Winsock], PHOSTENT, PHOSTENT structure pointer [Winsock], _win32_hostent_2, hostent, hostent structure [Winsock], winsock.hostent_2, winsock/FAR *LPHOSTENT, winsock/PHOSTENT, winsock/hostent"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: HOSTENT, *PHOSTENT, *LPHOSTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock.h
api_name:
 - HOSTENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# hostent structure


## -description


The 
<b>hostent</b> structure is used by functions to store information about a given host, such as host name, IPv4 address, and so forth. An application should never attempt to modify this structure or to free any of its components. Furthermore, only one copy of the 
<b>hostent</b> structure is allocated per thread, and an application should therefore copy any information that it needs before issuing any other Windows Sockets API calls.


## -struct-fields




### -field h_name

The official name of the host (PC). If using the DNS or similar resolution system, it is the Fully Qualified Domain Name (FQDN) that caused the server to return a reply. If using a local hosts file, it is the first entry after the IPv4 address.


### -field h_aliases

A <b>NULL</b>-terminated array of alternate names.


### -field h_addrtype

The type of address being returned.


### -field h_length

The length, in bytes, of each address.


### -field h_addr_list

A <b>NULL</b>-terminated list of addresses for the host. Addresses are returned in network byte order. The macro <b>h_addr</b> is defined to be <code>h_addr_list[0]</code> for compatibility with older software.


## -remarks



The 
<a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a> and <a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a> functions returns a pointer to a 
<b>hostent</b> structure—a structure allocated by Windows Sockets. The 
<b>hostent</b> structure contains the results of a successful search for the host specified in the <i>name</i> parameter. 

The memory for the <b>hostent</b> structure  returned by the <a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a> and <a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a> functions is allocated internally by the Winsock DLL from thread local storage. Only a single <b>hostent</b> structure is allocated and used, no matter how many times the <b>gethostbyaddr</b> or <b>gethostbyname</b> functions are called on the thread. The returned  <b>hostent</b> structure  must be copied to an application buffer if additional calls are to be made to the <b>gethostbyaddr</b> or <b>gethostbyname</b> functions on the same thread. Otherwise, the return value will be overwritten by subsequent <b>gethostbyaddr</b> or <b>gethostbyname</b> calls on the same thread. The internal memory allocated for the returned  <b>hostent</b> structure is released by the Winsock DLL when the thread exits. 

An application should not try to release the memory used by the returned <b>hostent</b> structure. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other function calls to <a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a> or <a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a>.


#### Examples

The following examples demonstrates the use of the <b>hostent</b> structure with the <a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define WIN32_LEAN_AND_MEAN

#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;stdio.h&gt;

// Need to link with Ws2_32.lib
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
        printf("usage: %s ipv4address\n", argv[0]);
        printf(" or\n");
        printf("       %s hostname\n", argv[0]);
        printf("  to return the host\n");
        printf("       %s 127.0.0.1\n", argv[0]);
        printf("  to return the IP addresses for a host\n");
        printf("       %s www.contoso.com\n", argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    host_name = argv[1];

// If the user input is an alpha name for the host, use gethostbyname()
// If not, get host by addr (assume IPv4)
    if (isalpha(host_name[0])) {        /* host address is a name */
        printf("Calling gethostbyname with %s\n", host_name);
        remoteHost = gethostbyname(host_name);
    } else {
        printf("Calling gethostbyaddr with %s\n", host_name);
        addr.s_addr = inet_addr(host_name);
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



## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/82436a88-5b37-4758-a5c9-b60dd1cbc36c">GetAddrInfoW</a>



<a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a>



<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>



<a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>



<a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a>



<a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a>
 

 

