---
UID: NF:wsipv6ok.gethostbyname
title: gethostbyname macro
author: windows-sdk-content
description: The gethostbyname function retrieves host information corresponding to a host name from a host database.
old-location: winsock\gethostbyname_2.htm
old-project: winsock
ms.assetid: 2526ecb5-927b-40c8-8d8f-919e7986ff05
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: "_win32_gethostbyname_2, gethostbyname, gethostbyname function [Winsock], winsock.gethostbyname_2, wsipv6ok/gethostbyname"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: wsipv6ok.h
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
 - gethostbyname
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# gethostbyname macro


## -description


The 
<b>gethostbyname</b> function retrieves host information corresponding to a host name from a host database.


<div class="alert"><b>Note</b>  The 
<b>gethostbyname</b> function has been deprecated by the introduction of the 
<a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a> function. Developers creating Windows Sockets 2 applications are urged to use the 
<b>getaddrinfo</b> function instead of 
<b>gethostbyname</b>.</div>
<div> </div>



## -parameters




### -param a

TBD






#### - name [in]

A pointer to the <b>null</b>-terminated name of the host to resolve.


## -remarks



The 
<b>gethostbyname</b> function returns a pointer to a 
<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure—a structure allocated by Windows Sockets. The 
<b>hostent</b> structure contains the results of a successful search for the host specified in the <i>name</i> parameter. 

If the host specified in the <i>name</i> parameter has both IPv4 and IPv6 addresses, only the IPv4 addresses will be returned. The  <b>gethostbyname</b> function can only return IPv4 addresses for the <i>name</i> parameter. The  <a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a> function and associated <a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a> structure should be used if IPv6 addresses for the host are required or if both IPv4 and IPv6 addresses for the host are required.

If the <i>name</i> parameter points to an empty string or <i>name</i> is <b>NULL</b>, the returned string is the same as the string returned by a successful 
<a href="https://msdn.microsoft.com/8fa40b60-0e93-493b-aee1-cea6cf595707">gethostname</a> function call (the standard host name for the local computer).

If the <i>name</i> parameter contains a string representation of a legal IPv4 address, then the binary IPv4 address that represents the string is returned in the <a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure. The <b>h_name</b> member of the <b>hostent</b> structure contains the string representation of the IPv4 address and the <b>h_addr_list</b>  contains the binary IPv4 address. If the <i>name</i> parameter contains a string representation of an IPv6 address or an illegal IPv4 address, then the  <b>gethostbyname</b> function will fail and return <a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANO_DATA</a>.  

The memory for the <a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure  returned by the <b>gethostbyname</b> function is allocated internally by the Winsock DLL from thread local storage. Only a single <b>hostent</b> structure is allocated and used, no matter how many times the <a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a> 
		 or <b>gethostbyname</b> functions are called on the thread. The returned  <b>hostent</b> structure  must be copied to an application buffer if additional calls are to be made to the <b>gethostbyname</b> or <b>gethostbyaddr</b> functions on the same thread. Otherwise, the return value will be overwritten by subsequent <b>gethostbyname</b> or <b>gethostbyaddr</b> 
		 calls on the same thread. The internal memory allocated for the returned  <b>hostent</b> structure is released by the Winsock DLL when the thread exits. 

An application should not try to release the memory used by the returned <a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a> structure. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other function calls to <b>gethostbyname</b> or <a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a> 
		.

The 
<b>gethostbyname</b> function cannot take an IP address string as a parameter passed to it in the <i>name</i> and resolve it to a host name. Such a request is treated exactly as a string representation of an IPv4 address or an unknown host name were passed. An application can use the <a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a> to convert an IPv4 address string to a binary IPv4 address, then use another function, 
<a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a>, to resolve the IPv4 address to a host name.  


<div class="alert"><b>Note</b>  The <b>gethostbyname</b> function does not check the size of the <i>name</i> parameter before passing the buffer. With an improperly sized <i>name</i> parameter, heap corruption can occur.</div>
<div> </div>


<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following examples demonstrates the use of the <b>gethostbyname</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;stdio.h&gt;
#include &lt;windows.h&gt;
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
    iResult = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
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
        printf("\tOfficial name: %s\n", remoteHost-&gt;h_name);
        for (pAlias = remoteHost-&gt;h_aliases; *pAlias != 0; pAlias++) {
            printf("\tAlternate name #%d: %s\n", ++i, *pAlias);
        }
        printf("\tAddress type: ");
        switch (remoteHost-&gt;h_addrtype) {
        case AF_INET:
            printf("AF_INET\n");
            break;
        case AF_NETBIOS:
            printf("AF_NETBIOS\n");
            break;
        default:
            printf(" %d\n", remoteHost-&gt;h_addrtype);
            break;
        }
        printf("\tAddress length: %d\n", remoteHost-&gt;h_length);

        i = 0;
        if (remoteHost-&gt;h_addrtype == AF_INET)
        {
            while (remoteHost-&gt;h_addr_list[i] != 0) {
                addr.s_addr = *(u_long *) remoteHost-&gt;h_addr_list[i++];
                printf("\tIP Address #%d: %s\n", i, inet_ntoa(addr));
            }
        }
        else if (remoteHost-&gt;h_addrtype == AF_NETBIOS)
        {   
            printf("NETBIOS address was returned\n");
        }   
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



<a href="https://msdn.microsoft.com/1a2b9c76-6e84-4ac2-b5c1-a2268edd0c49">WSAAsyncGetHostByName</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a>



<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>



<a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>



<a href="https://msdn.microsoft.com/303023e1-a486-4457-80f6-8aa80f6b2c79">gethostbyaddr</a>



<a href="https://msdn.microsoft.com/8fa40b60-0e93-493b-aee1-cea6cf595707">gethostname</a>



<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>
 

 

