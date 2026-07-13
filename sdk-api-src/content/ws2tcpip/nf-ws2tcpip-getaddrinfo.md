---
UID: NF:ws2tcpip.getaddrinfo
title: getaddrinfo function (ws2tcpip.h)
description: Provides protocol-independent translation from an ANSI host name to an address.
helpviewer_keywords: ["GetAddrInfoA","_win32_getaddrinfo_2","getaddrinfo","getaddrinfo function [Winsock]","winsock.getaddrinfo_2","ws2tcpip/getaddrinfo"]
old-location: winsock\getaddrinfo_2.htm
tech.root: WinSock
ms.assetid: 7034b866-346e-4a3b-b81b-72816d95b1d6
ms.date: 12/05/2018
ms.keywords: GetAddrInfoA, _win32_getaddrinfo_2, getaddrinfo, getaddrinfo function [Winsock], winsock.getaddrinfo_2, ws2tcpip/getaddrinfo
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 8.1 [desktop apps \| UWP apps]
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
 - getaddrinfo
 - ws2tcpip/getaddrinfo
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
 - getaddrinfo
---

# getaddrinfo function


## -description

The 
<b>getaddrinfo</b> function provides protocol-independent translation from an ANSI host name to an address.

## -parameters

### -param pNodeName [in, optional]

A pointer to a <b>NULL</b>-terminated ANSI string that contains a host (node) name or a numeric host address string. For the Internet protocol, the numeric host address string is a dotted-decimal IPv4 address or an IPv6 hex address.

### -param pServiceName [in, optional]

A pointer to a <b>NULL</b>-terminated ANSI string that contains either a service name or port number represented as a string.

A service name is a string alias for a port number. For example, “http” is an alias for port 80 defined by the Internet Engineering Task Force (IETF) as the default port used by web servers for the HTTP protocol. Possible values for the <i>pServiceName</i> parameter when a port number is not specified are listed in the following file: 

<code>%WINDIR%\system32\drivers\etc\services</code>

### -param pHints [in, optional]

A pointer to an 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure that provides hints about the type of socket the caller supports. 

The <b>ai_addrlen</b>, <b>ai_canonname</b>, <b>ai_addr</b>, and <b>ai_next</b> members of the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure pointed to by the <i>pHints</i> parameter must be zero or <b>NULL</b>. Otherwise the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function will fail with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a>.

See the Remarks for more details.

### -param ppResult [out]

A pointer to a linked list of one or more 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structures that contains response information about the host.

## -returns

Success returns zero. Failure returns a nonzero Windows Sockets error code, as found in the 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>.

Most nonzero error codes returned by the 
<b>getaddrinfo</b> function map to the set of errors outlined by Internet Engineering Task Force (IETF) recommendations. The following table lists these error codes and their WSA equivalents. It is recommended that the WSA error codes be used, as they offer familiar and comprehensive error information for Winsock programmers.

<table>
<tr>
<th>Error value</th>
<th>WSA equivalent</th>
<th>Description</th>
</tr>
<tr>
<td>EAI_AGAIN</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></td>
<td>A temporary failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_BADFLAGS</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></td>
<td>An invalid value was provided for the <b>ai_flags</b> member of the <i>pHints</i> parameter.</td>
</tr>
<tr>
<td>EAI_FAIL</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></td>
<td>A nonrecoverable failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_FAMILY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></td>
<td>The <b>ai_family</b> member of the <i>pHints</i> parameter is not supported.</td>
</tr>
<tr>
<td>EAI_MEMORY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></td>
<td>A memory allocation failure occurred.</td>
</tr>
<tr>
<td>EAI_NONAME</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></td>
<td>The name does not resolve for the supplied parameters or the <i>pNodeName</i> and <i>pServiceName</i> parameters were not provided.</td>
</tr>
<tr>
<td>EAI_SERVICE</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATYPE_NOT_FOUND</a></td>
<td>The <i>pServiceName</i> parameter is not supported for the specified <b>ai_socktype</b> member of the <i>pHints</i> parameter.</td>
</tr>
<tr>
<td>EAI_SOCKTYPE</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESOCKTNOSUPPORT</a></td>
<td>The <b>ai_socktype</b> member of the <i>pHints</i> parameter is not supported.</td>
</tr>
</table>
 

Use the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a> function to print error messages based on the EAI codes returned by the 
<b>getaddrinfo</b> function. The 
<b>gai_strerror</b> function is provided for compliance with IETF recommendations, but it is not thread safe. Therefore, use of traditional Windows Sockets functions such as 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> is recommended.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
An address incompatible with the requested protocol was used. This error is returned if the <b>ai_family</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure pointed to by the <i>pHints</i> parameter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was supplied.  This error is returned if an invalid value was provided for the <b>ai_flags</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure pointed to by the <i>pHints</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESOCKTNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The support for the specified socket type does not exist in this address family. This error is returned if the <b>ai_socktype</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure pointed to by the <i>pHints</i> parameter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
No such host is known. This error is returned if the name does not resolve for the supplied parameters or the <i>pNodeName</i> and <i>pServiceName</i> parameters were not provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The requested name is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred during a database lookup. This error is returned if nonrecoverable error in name resolution occurred.

</td>
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server. This error is returned when a temporary failure in name resolution occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATYPE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The specified class was not found. The <i>pServiceName</i> parameter is not supported for the specified <b>ai_socktype</b> member of the 
			<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure pointed to by the <i>pHints</i> parameter.

</td>
</tr>
</table>

## -remarks

The <b>getaddrinfo</b> function is the ANSI version of a function that provides protocol-independent translation from host name to address. The Unicode version of this function is <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>. Developers are encouraged to use the <b>GetAddrInfoW</b> Unicode function rather than the <b>getaddrinfo</b> ANSI function.

The <b>getaddrinfo</b> function returns results for the <b>NS_DNS</b> namespace. The <b>getaddrinfo</b> function aggregates all responses if more than
    one namespace provider returns information. For use with the IPv6 and IPv4 protocol, name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, or by other naming mechanisms for the <b>NS_DNS</b> namespace. 

Another name that can be used for the <b>getaddrinfo</b> function is <b>GetAddrInfoA</b>. Macros in the <i>Ws2tcpip.h</i> header file define <b>GetAddrInfoA</b> to <b>getaddrinfo</b>.

Macros in the <i>Ws2tcpip.h</i> header file define a mixed-case function name of <b>GetAddrInfo</b> and a <b>ADDRINFOT</b> structure. This <b>GetAddrInfo</b> function should be called with the <i>pNodeName</i> and <i>pServiceName</i> parameters of a pointer of type  <b>TCHAR</b> and the <i>pHints</i> and <i>ppResult</i> parameters of a pointer of type <b>ADDRINFOT</b>. When UNICODE or _UNICODE is not defined, <b>GetAddrInfo</b> is defined to <b>getaddrinfo</b>, the ANSI version of the function, and  <b>ADDRINFOT</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure. When <b>UNICODE</b> or <b>_UNICODE</b> is defined, <b>GetAddrInfo</b> is defined to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>, the Unicode version of the function, and  <b>ADDRINFOT</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a> structure.

The parameter names and parameter types for the <b>getaddrinfo</b> function defined in the <i>Ws2tcpip.h</i> header file on the Platform Software Development Kit (SDK) for   Windows Server 2003, and Windows XP were different. 

One or both of the <i>pNodeName</i> or <i>pServiceName</i> parameters must point to a <b>NULL</b>-terminated ANSI string; generally both are provided.

Upon success, a linked list of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structures is returned in the <i>ppResult</i> parameter. The list can be processed by following the pointer provided in the <b>ai_next</b> member of each returned 
<b>addrinfo</b> structure until a <b>NULL</b> pointer is encountered. In each returned 
<b>addrinfo</b> structure, the <b>ai_family</b>, <b>ai_socktype</b>, and <b>ai_protocol</b> members correspond to respective arguments in a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>   or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> function call. Also, the <b>ai_addr</b> member in each returned 
<b>addrinfo</b> structure points to a filled-in socket address structure, the length of which is specified in its <b>ai_addrlen</b> member.

If the <i>pNodeName</i> parameter points to a computer name, all permanent addresses for the computer that can be used as a source address are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> or <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to false in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure. 

If the <i>pNodeName</i> parameter points to a string equal to "localhost", all loopback addresses on the local computer are returned. 

If the <i>pNodeName</i> parameter contains an empty string, all registered addresses on the local computer are returned. 

On Windows Server 2003 and later if the <i>pNodeName</i> parameter points to a string equal to "..localmachine", all registered addresses on the local computer are returned. 

If the <i>pNodeName</i> parameter refers to a cluster virtual server name, only virtual server addresses are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> or <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to true in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure. See <a href="/previous-versions/windows/desktop/mscs/windows-clustering">Windows Clustering</a> for more information about clustering.

Windows 7 with Service Pack 1 (SP1) and Windows Server 2008 R2 with Service Pack 1 (SP1) add support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This also changes the behavior such that if the <b>SkipAsSource</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  

A hotfix is available for Windows 7 and Windows Server 2008 R2 that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address.  This hotfix also changes behavior such that if the <b>SkipAsSource</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  For more information, see <a href="https://support.microsoft.com/kb/2386184">Knowledge Base (KB) 2386184</a>.   

A similar hotfix is also available for Windows Vista with Service Pack 2 (SP2) and Windows Server 2008 with Service Pack 2 (SP2) that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This hotfix also changes behavior such that if the <b>SkipAsSource</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS. 


Callers of the 
<b>getaddrinfo</b> function can provide hints about the type of socket supported through an 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure pointed to by the <i>pHints</i> parameter. When the <i>pHints</i> parameter is used, the following rules apply to its associated 
<b>addrinfo</b> structure:

<ul>
<li>A value of <b>AF_UNSPEC</b> for <b>ai_family</b> indicates the caller will accept only the <b>AF_INET</b> and <b>AF_INET6</b> address families. Note that <b>AF_UNSPEC</b> and <b>PF_UNSPEC</b> are the same.</li>
<li>A value of zero for <b>ai_socktype</b> indicates the caller will accept any socket type.</li>
<li>A value of zero for <b>ai_protocol</b> indicates the caller will accept any protocol.</li>
<li>The <b>ai_addrlen</b> member must be set to zero.</li>
<li>The <b>ai_canonname</b> member must be set to <b>NULL</b>.</li>
<li>The <b>ai_addr</b> member must be set to <b>NULL</b>.</li>
<li>The <b>ai_next</b> member must be set to <b>NULL</b>.</li>
</ul>


A value of <b>AF_UNSPEC</b> for <b>ai_family</b> indicates the caller will accept any protocol family. This value can be used to return both IPv4 and IPv6 addresses for the host name pointed to by the <i>pNodeName</i> parameter. On Windows Server 2003 and Windows XP, IPv6 addresses are returned only if IPv6 is installed on the local computer. 

Other values in the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure provided in the <i>pHints</i> parameter indicate specific requirements. For example, if the caller handles only IPv4 and does not handle IPv6, the <b>ai_family</b> member should be set to AF_INET. For another example, if the caller handles only TCP and does not handle UDP, the <b>ai_socktype</b> member should be set to <b>SOCK_STREAM</b>.

If the <i>pHints</i> parameter is a <b>NULL</b> pointer, the 
<b>getaddrinfo</b> function treats it as if the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure in <i>pHints</i> were initialized with its <b>ai_family</b> member set to <b>AF_UNSPEC</b> and all other members set to zero.

On Windows Vista and later when <b>getaddrinfo</b> is called from a service, if the operation is the result of a user process calling the service, then the service should impersonate the user.  This is to allow security to be properly enforced.


The 
<b>getaddrinfo</b> function can be used to convert a text string representation of an IP address to an <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure that contains a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure for the IP address and other information. To be used in this way, the string pointed to by the <i>pNodeName</i> parameter must contain a text representation of an IP address and the <b>addrinfo</b> structure pointed to by the <i>pHints</i> parameter must have the AI_NUMERICHOST flag set in the <b>ai_flags</b> member. The string pointed to by the <i>pNodeName</i> parameter may contain a text representation of either an IPv4 or an IPv6 address. The text IP address is converted to an <b>addrinfo</b> structure pointed to by the <i>ppResult</i> parameter. The returned <b>addrinfo</b> structure contains a <b>sockaddr</b> structure for the IP address along with addition information about the IP address. For this method to work with an IPv6 address string on Windows Server 2003 and Windows XP, the IPv6 protocol must be installed on the local computer. Otherwise, the <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a> error is returned.

<h3><a id="Freeing_Address_Information_from_Dynamic_Allocation"></a><a id="freeing_address_information_from_dynamic_allocation"></a><a id="FREEING_ADDRESS_INFORMATION_FROM_DYNAMIC_ALLOCATION"></a>Freeing Address Information from Dynamic Allocation</h3>
All information returned by the 
<b>getaddrinfo</b> function pointed to by the <i>ppResult</i> parameter is dynamically allocated, including all 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structures, socket address structures, and canonical host name strings pointed to by 
<b>addrinfo</b> structures. Memory allocated by a successful call to this function must be released with a subsequent call to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfo">freeaddrinfo</a>.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following code example shows how to use the <b>getaddrinfo</b> function.


```cpp
#undef UNICODE

#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

// link with Ws2_32.lib
#pragma comment (lib, "Ws2_32.lib")

int __cdecl main(int argc, char **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;
    INT iRetval;

    DWORD dwRetval;

    int i = 1;
    
    struct addrinfo *result = NULL;
    struct addrinfo *ptr = NULL;
    struct addrinfo hints;

    struct sockaddr_in  *sockaddr_ipv4;
//    struct sockaddr_in6 *sockaddr_ipv6;
    LPSOCKADDR sockaddr_ip;

    char ipstringbuffer[46];
    DWORD ipbufferlength = 46;

    // Validate the parameters
    if (argc != 3) {
        printf("usage: %s <hostname> <servicename>\n", argv[0]);
        printf("getaddrinfo provides protocol-independent translation\n");
        printf("   from an ANSI host name to an IP address\n");
        printf("%s example usage\n", argv[0]);
        printf("   %s www.contoso.com 0\n", argv[0]);
        return 1;
    }

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    //--------------------------------
    // Setup the hints address info structure
    // which is passed to the getaddrinfo() function
    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    printf("Calling getaddrinfo with following parameters:\n");
    printf("\tnodename = %s\n", argv[1]);
    printf("\tservname (or port) = %s\n\n", argv[2]);
    
//--------------------------------
// Call getaddrinfo(). If the call succeeds,
// the result variable will hold a linked list
// of addrinfo structures containing response
// information
    dwRetval = getaddrinfo(argv[1], argv[2], &hints, &result);
    if ( dwRetval != 0 ) {
        printf("getaddrinfo failed with error: %d\n", dwRetval);
        WSACleanup();
        return 1;
    }

    printf("getaddrinfo returned success\n");
    
    // Retrieve each address and print out the hex bytes
    for(ptr=result; ptr != NULL ;ptr=ptr->ai_next) {

        printf("getaddrinfo response %d\n", i++);
        printf("\tFlags: 0x%x\n", ptr->ai_flags);
        printf("\tFamily: ");
        switch (ptr->ai_family) {
            case AF_UNSPEC:
                printf("Unspecified\n");
                break;
            case AF_INET:
                printf("AF_INET (IPv4)\n");
                sockaddr_ipv4 = (struct sockaddr_in *) ptr->ai_addr;
                printf("\tIPv4 address %s\n",
                    inet_ntoa(sockaddr_ipv4->sin_addr) );
                break;
            case AF_INET6:
                printf("AF_INET6 (IPv6)\n");
                // the InetNtop function is available on Windows Vista and later
                // sockaddr_ipv6 = (struct sockaddr_in6 *) ptr->ai_addr;
                // printf("\tIPv6 address %s\n",
                //    InetNtop(AF_INET6, &sockaddr_ipv6->sin6_addr, ipstringbuffer, 46) );
                
                // We use WSAAddressToString since it is supported on Windows XP and later
                sockaddr_ip = (LPSOCKADDR) ptr->ai_addr;
                // The buffer length is changed by each call to WSAAddresstoString
                // So we need to set it for each iteration through the loop for safety
                ipbufferlength = 46;
                iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr->ai_addrlen, NULL, 
                    ipstringbuffer, &ipbufferlength );
                if (iRetval)
                    printf("WSAAddressToString failed with %u\n", WSAGetLastError() );
                else    
                    printf("\tIPv6 address %s\n", ipstringbuffer);
                break;
            case AF_NETBIOS:
                printf("AF_NETBIOS (NetBIOS)\n");
                break;
            default:
                printf("Other %ld\n", ptr->ai_family);
                break;
        }
        printf("\tSocket type: ");
        switch (ptr->ai_socktype) {
            case 0:
                printf("Unspecified\n");
                break;
            case SOCK_STREAM:
                printf("SOCK_STREAM (stream)\n");
                break;
            case SOCK_DGRAM:
                printf("SOCK_DGRAM (datagram) \n");
                break;
            case SOCK_RAW:
                printf("SOCK_RAW (raw) \n");
                break;
            case SOCK_RDM:
                printf("SOCK_RDM (reliable message datagram)\n");
                break;
            case SOCK_SEQPACKET:
                printf("SOCK_SEQPACKET (pseudo-stream packet)\n");
                break;
            default:
                printf("Other %ld\n", ptr->ai_socktype);
                break;
        }
        printf("\tProtocol: ");
        switch (ptr->ai_protocol) {
            case 0:
                printf("Unspecified\n");
                break;
            case IPPROTO_TCP:
                printf("IPPROTO_TCP (TCP)\n");
                break;
            case IPPROTO_UDP:
                printf("IPPROTO_UDP (UDP) \n");
                break;
            default:
                printf("Other %ld\n", ptr->ai_protocol);
                break;
        }
        printf("\tLength of this sockaddr: %d\n", ptr->ai_addrlen);
        printf("\tCanonical name: %s\n", ptr->ai_canonname);
    }

    freeaddrinfo(result);
    WSACleanup();

    return 0;
}

```



<div class="alert"><b>Note</b>  Ensure that the development environment targets the newest version of <i>Ws2tcpip.h</i> which includes structure and function definitions for <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> and <b>getaddrinfo</b>, respectively.</div>
<div> </div>


<h3><a id="IDNs"></a><a id="idns"></a><a id="IDNS"></a>Internationalized Domain Names</h3>
Internet host names typically consist of a very restricted set of characters: 



<ul>
<li>Upper and lower case ASCII letters from the English alphabet.
</li>
<li>Digits from 0 to 9.</li>
<li>ASCII hyphen characters.
</li>
</ul>


With the growth of the Internet, there is a growing need to identify Internet host names for other languages not represented by the ASCII character set. Identifiers which facilitate this need and allow non-ASCII characters (Unicode) to be represented as special ASCII character strings are known as Internationalized Domain Names (IDNs). A  mechanism called
   Internationalizing Domain Names in Applications (IDNA) is used to handle
   IDNs in a standard fashion.  The specifications for IDNs and IDNA are documented in <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>, <a href="http://tools.ietf.org/html/rfc5890">RTF 5890</a>, and <a href="http://tools.ietf.org/html/rfc6365">RFC 6365</a> published by the Internet Engineering Task Force (IETF).


On Windows 8 and Windows Server 2012, the <b>getaddrinfo</b> function provides support for Internationalized Domain Name (IDN) parsing applied to the name passed in the <i>pNodeName</i> parameter. Winsock performs Punycode/IDN encoding and conversion.  This behavior can be disabled using the <b>AI_DISABLE_IDN_ENCODING</b> flag discussed below.

On Windows 7 and Windows Server 2008 R2 or earlier, the <b>getaddrinfo</b> function does not currently provide support IDN parsing applied to the name passed in the <i>pNodeName</i> parameter. Winsock does not perform any Punycode/IDN conversion.  The wide character version of the <b>GetAddrInfo</b> function does not use Punycode to convert an IDN as per <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>. The wide character version of the <b>GetAddrInfo</b> function when querying DNS encodes the Unicode name in UTF-8 format, the format used by Microsoft DNS servers in an enterprise environment.

Several functions on Windows Vista and later support conversion between Unicode labels in an IDN to their ASCII equivalents. The resulting representation of each  Unicode label contains only ASCII characters and starts with the xn-- prefix if the Unicode label contained any non-ASCII characters. The reason for this is to support existing DNS servers on the Internet, since some DNS tools and servers only support ASCII characters (see <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>). 

 

The <a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a> function uses Punycode to convert an IDN to the ASCII representation of the original Unicode string using the standard algorithm defined in <a href="http://tools.ietf.org/html/rfc3490">RFC 3490</a>. The <a href="/windows/desktop/api/winnls/nf-winnls-idntounicode">IdnToUnicode</a> function converts the ASCII form of an IDN to the normal Unicode UTF-16 encoding syntax. For more information and links to related draft standards, see <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>.



The <a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a> function can be used to convert an IDN name to the ASCII form that then can be passed in the <i>pNodeName</i> parameter to the <b>getaddrinfo</b> function. To pass this IDN name to the  <b>GetAddrInfo</b> function when the wide character version of this function is used (when UNICODE or _UNICODE is defined), you can use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> function to convert the <b>CHAR</b> string into a <b>WCHAR</b> string. 

<h3><a id="ai_flags"></a><a id="AI_FLAGS"></a>Use of ai_flags in the pHints parameter</h3>


Flags in the <b>ai_flags</b> member of the optional 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure provided in the <i>pHints</i> parameter modify the behavior of the function. 

These flag bits are defined in the <i>Ws2def.h</i> header file on the Microsoft Windows Software Development Kit (SDK) for Windows 7. These flag bits are defined in the <i>Ws2tcpip.h</i> header file on the Windows SDK for Windows Server 2008 and Windows Vista.  These flag bits are defined in the <i>Ws2tcpip.h</i> header file on the Platform SDK for   Windows Server 2003, and Windows XP. 

The flag bits can be a combination of the following: 



<table>
<tr>
<th>Flag Bits</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="AI_PASSIVE"></a><a id="ai_passive"></a><b>AI_PASSIVE</b>

</td>
<td width="60%">
Setting the <b>AI_PASSIVE</b> flag indicates the caller intends to use the returned socket address structure in a call to the 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function. When the <b>AI_PASSIVE</b> flag is set and <i>pNodeName</i> is a <b>NULL</b> pointer, the IP address portion of the socket address structure is set to <b>INADDR_ANY</b> for IPv4 addresses and <b>IN6ADDR_ANY_INIT</b> for IPv6 addresses.

When the <b>AI_PASSIVE</b> flag is not set, the returned socket address structure is ready for a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> function for a connection-oriented protocol, or ready for a call to either the 
<b>connect</b>, 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> functions for a connectionless protocol. If the <i>pNodeName</i> parameter is a <b>NULL</b> pointer in this case, the IP address portion of the socket address structure is set to the loopback address.

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_CANONNAME"></a><a id="ai_canonname"></a><b>AI_CANONNAME</b>

</td>
<td width="60%">
If neither <b>AI_CANONNAME</b> nor <b>AI_NUMERICHOST</b> is used, the 
<b>getaddrinfo</b> function attempts resolution. If a literal string is passed 
<b>getaddrinfo</b> attempts to convert the string, and if a host name is passed the 
<b>getaddrinfo</b> function attempts to resolve the name to an address or multiple addresses.

When the <b>AI_CANONNAME</b> bit is set, the <i>pNodeName</i> parameter cannot be <b>NULL</b>. Otherwise the 
<b>getaddrinfo</b> function will  fail with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a>.

When the <b>AI_CANONNAME</b> bit is set and the 
<b>getaddrinfo</b> function returns success, the <b>ai_canonname</b> member in the <i>ppResult</i> parameter points to a <b>NULL</b>-terminated string that contains the canonical name of the specified node.

<div class="alert"><b>Note</b>  The <b>getaddrinfo</b> function can return success when the <b>AI_CANONNAME</b> flag is set, yet the <b>ai_canonname</b> member in the associated 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure is <b>NULL</b>. Therefore, the recommended use of the <b>AI_CANONNAME</b> flag includes testing whether the <b>ai_canonname</b> member in the associated 
<b>addrinfo</b> structure is <b>NULL</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<a id="AI_NUMERICHOST"></a><a id="ai_numerichost"></a><b>AI_NUMERICHOST</b>

</td>
<td width="60%">
When the <b>AI_NUMERICHOST</b> bit is set, the <i>pNodeName</i> parameter must contain a non-<b>NULL</b> numeric host address string, otherwise the <b>EAI_NONAME</b> error is returned. This flag prevents a name resolution service from being called. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_NUMERICSERV"></a><a id="ai_numericserv"></a><b>AI_NUMERICSERV</b>

</td>
<td width="60%">
When the <b>AI_NUMERICSERV</b> bit is set, the <i>pServiceName</i> parameter must contain a non-<b>NULL</b> numeric port number, otherwise the <b>EAI_NONAME</b> error is returned. This flag prevents a name resolution service from being called. 

The <b>AI_NUMERICSERV</b> flag is defined on Windows SDK for Windows Vista and later.  The <b>AI_NUMERICSERV</b> flag is not supported by Microsoft providers. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_ALL"></a><a id="ai_all"></a><b>AI_ALL</b>

</td>
<td width="60%">
If the  <b>AI_ALL</b> bit is set, a request is made for IPv6 addresses and IPv4 addresses with <b>AI_V4MAPPED</b>. 

The <b>AI_ALL</b> flag is defined on the Windows SDK for Windows Vista and later. The <b>AI_ALL</b> flag is supported on   Windows Vista and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_ADDRCONFIG"></a><a id="ai_addrconfig"></a><b>AI_ADDRCONFIG</b>

</td>
<td width="60%">
If the <b>AI_ADDRCONFIG</b> bit is set, <b>getaddrinfo</b> will resolve only if a global address is configured. If <b>AI_ADDRCONFIG</b> flag is specified, IPv4 addresses shall be
   returned only if an IPv4 address is configured on the local system,
   and IPv6 addresses shall be returned only if an IPv6 address is
   configured on the local system.  The IPv4 or IPv6 loopback address is not
   considered a valid global address.

The <b>AI_ADDRCONFIG</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_ADDRCONFIG</b> flag is supported on   Windows Vista and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_V4MAPPED"></a><a id="ai_v4mapped"></a><b>AI_V4MAPPED</b>

</td>
<td width="60%">
If the  <b>AI_V4MAPPED</b> bit is set and a request for IPv6 addresses fails, a name service request is made for IPv4 addresses and these addresses are converted to IPv4-mapped IPv6 address format.

The <b>AI_V4MAPPED</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_V4MAPPED</b> flag is supported on   Windows Vista and later. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_NON_AUTHORITATIVE"></a><a id="ai_non_authoritative"></a><b>AI_NON_AUTHORITATIVE</b>

</td>
<td width="60%">
If the  <b>AI_NON_AUTHORITATIVE</b> bit is set, the <b>NS_EMAIL</b> namespace provider returns both authoritative and non-authoritative results. If the  <b>AI_NON_AUTHORITATIVE</b> bit is not set, the <b>NS_EMAIL</b> namespace provider returns only authoritative results. 

The <b>AI_NON_AUTHORITATIVE</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_NON_AUTHORITATIVE</b> flag is supported on Windows Vista and later and applies only to the <b>NS_EMAIL</b> namespace. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_SECURE"></a><a id="ai_secure"></a><b>AI_SECURE</b>

</td>
<td width="60%">
If the  <b>AI_SECURE</b> bit is set, the <b>NS_EMAIL</b> namespace provider will return results that were obtained with enhanced security to minimize possible spoofing.

The <b>AI_SECURE</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_SECURE</b> flag is supported on Windows Vista and later and applies only to the <b>NS_EMAIL</b> namespace. 



</td>
</tr>
<tr>
<td width="40%">
<a id="AI_RETURN_PREFERRED_NAMES"></a><a id="ai_return_preferred_names"></a><b>AI_RETURN_PREFERRED_NAMES</b>

</td>
<td width="60%">
If the  <b>AI_RETURN_PREFERRED_NAMES</b> is set, then no name should be provided in the <i>pNodeName</i> parameter. The <b>NS_EMAIL</b> namespace provider will return preferred names for publication.

The <b>AI_RETURN_PREFERRED_NAMES</b> flag is defined on the Windows SDK for  Windows Vista and later.    The <b>AI_RETURN_PREFERRED_NAMES</b> flag is supported on Windows Vista and later and applies only to the <b>NS_EMAIL</b> namespace. 

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_FQDN"></a><a id="ai_fqdn"></a><b>AI_FQDN</b>

</td>
<td width="60%">
If the  <b>AI_FQDN</b> is set and a flat name (single label) is specified,  <b>getaddrinfo</b> will return the fully qualified domain name that the name eventually resolved to. The fully qualified domain name is returned in the <b>ai_canonname</b> member in the associated 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure. This is different than <b>AI_CANONNAME</b> bit flag that returns the canonical name registered in DNS which may be different than the fully qualified domain name  that the flat name resolved to. Only one of the <b>AI_FQDN</b> and <b>AI_CANONNAME</b> bits can be set. The <b>getaddrinfo</b> function will fail if both flags are present with <b>EAI_BADFLAGS</b>.


When the <b>AI_FQDN</b> bit is set, the <i>pNodeName</i> parameter cannot be <b>NULL</b>. Otherwise the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function will  fail with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a>.

<b>Windows 7:  </b>The <b>AI_FQDN</b> flag is defined on the Windows SDK for  Windows 7 and later.    The <b>AI_FQDN</b> flag is supported on Windows 7 and later. 



</td>
</tr>
<tr>
<td width="40%">
<a id="AI_FILESERVER"></a><a id="ai_fileserver"></a><b>AI_FILESERVER</b>

</td>
<td width="60%">
If the  <b>AI_FILESERVER</b> is set, this is a  hint to the namespace provider that the hostname being queried is being used in file share scenario. The namespace provider may ignore this hint.


<b>Windows 7:  </b>The <b>AI_FILESERVER</b> flag is defined on the Windows SDK for  Windows 7 and later.    The <b>AI_FILESERVER</b> flag is supported on Windows 7 and later. 

</td>
</tr>
</table>
 



<h3><a id="Example_code_using_AI_NUMERICHOST"></a><a id="example_code_using_ai_numerichost"></a><a id="EXAMPLE_CODE_USING_AI_NUMERICHOST"></a>Example code using AI_NUMERICHOST</h3>
The following code example shows how to use the <b>getaddrinfo</b> function to convert a text string representation of an IP address to an <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure that contains a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure for the IP address and other information. 


```cpp
#undef UNICODE

#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

// link with Ws2_32.lib
#pragma comment (lib, "Ws2_32.lib")

int __cdecl main(int argc, char **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    DWORD dwRetval;

    int i = 1;
    
    struct addrinfo *result = NULL;
    struct addrinfo *ptr = NULL;
    struct addrinfo hints;


    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s <IP Address String>\n", argv[0]);
        printf("  getaddrinfo determines the IP binary network address\n");
        printf("       %s 207.46.197.32\n", argv[0]);  /* www.contoso.com */
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    //--------------------------------
    // Setup the hints address info structure
    // which is passed to the getaddrinfo() function
    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_flags = AI_NUMERICHOST;
    hints.ai_family = AF_UNSPEC;
//    hints.ai_socktype = SOCK_STREAM;
//    hints.ai_protocol = IPPROTO_TCP;


//--------------------------------
// Call getaddrinfo(). If the call succeeds,
// the result variable will hold a linked list
// of addrinfo structures containing response
// information
    dwRetval = getaddrinfo(argv[1], NULL, &hints, &result);
    if ( dwRetval != 0 ) {
        printf("getaddrinfo failed with error: %d\n", dwRetval);
        WSACleanup();
        return 1;
    }

    printf("getaddrinfo returned success\n");
    
    // Retrieve each address and print out the hex bytes
    for(ptr=result; ptr != NULL ;ptr=ptr->ai_next) {

        printf("getaddrinfo response %d\n", i++);
        printf("\tFlags: 0x%x\n", ptr->ai_flags);
        printf("\tFamily: ");
        switch (ptr->ai_family) {
            case AF_UNSPEC:
                printf("Unspecified\n");
                break;
            case AF_INET:
                printf("AF_INET (IPv4)\n");
                break;
            case AF_INET6:
                printf("AF_INET6 (IPv6)\n");
                break;
            case AF_NETBIOS:
                printf("AF_NETBIOS (NetBIOS)\n");
                break;
            default:
                printf("Other %ld\n", ptr->ai_family);
                break;
        }
        printf("\tSocket type: ");
        switch (ptr->ai_socktype) {
            case 0:
                printf("Unspecified\n");
                break;
            case SOCK_STREAM:
                printf("SOCK_STREAM (stream)\n");
                break;
            case SOCK_DGRAM:
                printf("SOCK_DGRAM (datagram) \n");
                break;
            case SOCK_RAW:
                printf("SOCK_RAW (raw) \n");
                break;
            case SOCK_RDM:
                printf("SOCK_RDM (reliable message datagram)\n");
                break;
            case SOCK_SEQPACKET:
                printf("SOCK_SEQPACKET (pseudo-stream packet)\n");
                break;
            default:
                printf("Other %ld\n", ptr->ai_socktype);
                break;
        }
        printf("\tProtocol: ");
        switch (ptr->ai_protocol) {
            case 0:
                printf("Unspecified\n");
                break;
            case IPPROTO_TCP:
                printf("IPPROTO_TCP (TCP)\n");
                break;
            case IPPROTO_UDP:
                printf("IPPROTO_UDP (UDP) \n");
                break;
            default:
                printf("Other %ld\n", ptr->ai_protocol);
                break;
        }
        printf("\tLength of this sockaddr: %d\n", ptr->ai_addrlen);
        printf("\tCanonical name: %s\n", ptr->ai_canonname);
    }

    freeaddrinfo(result);
    WSACleanup();

    return 0;
}

```


<h3><a id="Support_for_getaddrinfo_on_Windows_2000_and_older_versions_"></a><a id="support_for_getaddrinfo_on_windows_2000_and_older_versions_"></a><a id="SUPPORT_FOR_GETADDRINFO_ON_WINDOWS_2000_AND_OLDER_VERSIONS_"></a>Support for getaddrinfo on Windows 2000 and older versions
</h3>
The <b>getaddrinfo</b> function was added to the Ws2_32.dll on Windows XP and later. To execute an application that uses this function on earlier versions of Windows, then you need to include the <i>Ws2tcpip.h</i> and <i>Wspiapi.h</i> files. When the <i>Wspiapi.h</i> include file is added, the <b>getaddrinfo</b> function is defined to the <b>WspiapiGetAddrInfo</b> inline function in the <i>Wspiapi.h</i> file. At runtime, the <b>WspiapiGetAddrInfo</b> function is implemented in such a way that if the Ws2_32.dll or the Wship6.dll (the file containing <b>getaddrinfo</b> in the IPv6 Technology Preview for Windows 2000) does not include <b>getaddrinfo</b>, then a version of  <b>getaddrinfo</b> is implemented inline based on code in the Wspiapi.h header file. This inline code will be used on older Windows platforms that do not natively support the <b>getaddrinfo</b> function.

The IPv6  protocol is supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed. Otherwise <b>getaddrinfo</b> support on versions of Windows earlier than Windows XP is limited to handling IPv4 name resolution.

The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function is the Unicode version of  <b>getaddrinfo</b>.  The <b>GetAddrInfoW</b> function was added to the Ws2_32.dll in Windows XP with Service Pack 2 (SP2). The <b>GetAddrInfoW</b> function cannot be used on versions of Windows earlier than Windows XP with SP2. 



<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntounicode">IdnToUnicode</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoex2w">addrinfoex2</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfo">freeaddrinfo</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
