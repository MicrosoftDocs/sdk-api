---
UID: NF:ws2tcpip.GetAddrInfoW
title: GetAddrInfoW function
author: windows-sdk-content
description: Provides protocol-independent translation from a Unicode host name to an address.
old-location: winsock\getaddrinfow.htm
tech.root: winsock
ms.assetid: 82436a88-5b37-4758-a5c9-b60dd1cbc36c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetAddrInfoW, GetAddrInfoW function [Winsock], winsock.getaddrinfow, ws2tcpip/GetAddrInfoW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ws2tcpip.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - GetAddrInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetAddrInfoW
: 
---

# GetAddrInfoW function


## -description


The 
<b>GetAddrInfoW</b> function provides protocol-independent translation from a Unicode host name to an address.


## -parameters




### -param pNodeName [in, optional]

A pointer to a <b>NULL</b>-terminated Unicode string that contains a host (node) name or a numeric host address string. For the Internet protocol, the numeric host address string is a dotted-decimal IPv4 address or an IPv6 hex address.


### -param pServiceName [in, optional]

A pointer to a <b>NULL</b>-terminated Unicode string that contains either a service name or port number represented as a string. 

A service name is a string alias for a port number. For example, “http” is an alias for port 80 defined by the Internet Engineering Task Force (IETF) as the default port used by web servers for the HTTP protocol. Possible values for the <i>pServiceName</i> parameter when a port number is not specified are listed in the following file: 

<code>%WINDIR%\system32\drivers\etc\services</code>


### -param pHints [in, optional]

A pointer to an 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure that provides hints about the type of socket the caller supports. 

The <b>ai_addrlen</b>, <b>ai_canonname</b>, <b>ai_addr</b>, and <b>ai_next</b> members of the <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure pointed to by the <i>pHints</i> parameter must be zero or <b>NULL</b>. Otherwise the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function will fail with <a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a>.

See the Remarks for more details.


### -param ppResult [out]

A pointer to a linked list of one or more 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structures that contains response information about the host.


## -returns



Success returns zero. Failure returns a nonzero Windows Sockets error code, as found in the 
<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">Windows Sockets Error Codes</a>.

Most nonzero error codes returned by the <b>GetAddrInfoW</b> function map to the set of errors outlined by Internet Engineering Task Force (IETF) recommendations. The following table lists these error codes and their WSA equivalents. It is recommended that the WSA error codes be used, as they offer familiar and comprehensive error information for Winsock programmers.

<table>
<tr>
<th>Error value</th>
<th>WSA equivalent</th>
<th>Description</th>
</tr>
<tr>
<td>EAI_AGAIN</td>
<td><a href="windows_sockets_error_codes_2.htm">WSATRY_AGAIN</a></td>
<td>A temporary failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_BADFLAGS</td>
<td><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></td>
<td>An invalid value was provided for the <b>ai_flags</b> member of the <i>pHints</i> parameter.</td>
</tr>
<tr>
<td>EAI_FAIL</td>
<td><a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a></td>
<td>A nonrecoverable failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_FAMILY</td>
<td><a href="windows_sockets_error_codes_2.htm">WSAEAFNOSUPPORT</a></td>
<td>The <b>ai_family</b> member  of the <i>pHints</i> parameter is not supported.</td>
</tr>
<tr>
<td>EAI_MEMORY</td>
<td><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></td>
<td>A memory allocation failure occurred.</td>
</tr>
<tr>
<td>EAI_NONAME</td>
<td><a href="windows_sockets_error_codes_2.htm">WSAHOST_NOT_FOUND</a></td>
<td>The name does not resolve for the supplied parameters or the <i>pNodeName</i> and <i>pServiceName</i> parameters were not provided.</td>
</tr>
<tr>
<td>EAI_SERVICE</td>
<td><a href="windows_sockets_error_codes_2.htm">WSATYPE_NOT_FOUND</a></td>
<td>The <i>pServiceName</i> parameter is not supported for the specified <b>ai_socktype</b> member of the <i>pHints</i> parameter.</td>
</tr>
<tr>
<td>EAI_SOCKTYPE</td>
<td><a href="windows_sockets_error_codes_2.htm">WSAESOCKTNOSUPPORT</a></td>
<td>The <b>ai_socktype</b> member  of the <i>pHints</i> parameter is not supported.</td>
</tr>
</table>
 

Use the 
<a href="https://msdn.microsoft.com/00b4c5de-89c9-419f-bff8-822ef0446697">gai_strerror</a> function to print error messages based on the EAI_* codes returned by the 
<b>GetAddrInfoW</b> function. The 
<b>gai_strerror</b> function is provided for compliance with IETF recommendations, but it is not thread safe. Therefore, use of a traditional Windows Sockets function, such as 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>, is recommended.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
An address incompatible with the requested protocol was used. This error is returned if the <b>ai_family</b> member of the 
			<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>structure pointed to by the <i>hints</i> parameter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was supplied.  This error is returned if an invalid value was provided for the <b>ai_flags</b> member of the 
			<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>structure pointed to by the <i>hints</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAESOCKTNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The support for the specified socket type does not exist in this address family. This error is returned if the <b>ai_socktype</b> member of the 
			<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>structure pointed to by the <i>hints</i> parameter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
No such host is known. This error is returned if the name does not resolve for the supplied parameters or the <i>pNodename</i> and <i>pServicename</i> parameters were not provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The requested name is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred during a database lookup. This error is returned if nonrecoverable error in name resolution occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server. This error is returned when a temporary failure in name resolution occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSATYPE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The specified class was not found. The <i>pServiceName</i> parameter is not supported for the specified <b>ai_socktype</b> member of the 
			<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>structure pointed to by the <i>hints</i> parameter.

</td>
</tr>
</table>
 




## -remarks



The <b>GetAddrInfoW</b> function is the Unicode version of a function that provides protocol-independent translation from host name to address. The ANSI version of this function is <a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>.

The <b>GetAddrInfoW</b> function returns results for the <b>NS_DNS</b> namespace. The <b>GetAddrInfoW</b> function aggregates all responses if more than
    one namespace provider returns information. For use with the IPv6 and IPv4 protocol, name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, or by other naming mechanisms  for the <b>NS_DNS</b> namespace.

Macros in the Winsock header file define a mixed-case function name of <b>GetAddrInfo</b> and a <b>ADDRINFOT</b> structure. This <b>GetAddrInfo</b> function should be called with the <i>pNodeName</i> and <i>pServiceName</i> parameters of a pointer of type  <b>TCHAR</b> and the <i>pHints</i> and <i>ppResult</i> parameters of a pointer of type <b>ADDRINFOT</b>. When UNICODE or _UNICODE is defined, <b>GetAddrInfo</b> is defined to <b>GetAddrInfoW</b>, the Unicode version of the function, and <b>ADDRINFOT</b> is defined to the <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure. When UNICODE or _UNICODE is not defined, <b>GetAddrInfo</b> is defined to <a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>, the ANSI version of the function, and <b>ADDRINFOT</b> is defined to the <a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a> structure.

One or both of the <i>pNodeName</i> or <i>pServiceName</i> parameters must point to a <b>NULL</b>-terminated Unicode string; generally both are provided.

Upon success, a linked list of 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structures is returned in the <i>ppResult</i> parameter. The list can be processed by following the pointer provided in the <b>ai_next</b> member of each returned 
<b>addrinfoW</b> structure until a <b>NULL</b> pointer is encountered. In each returned 
<b>addrinfoW</b> structure, the <b>ai_family</b>, <b>ai_socktype</b>, and <b>ai_protocol</b> members correspond to respective arguments in a 
<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>  or <a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> function call. Also, the <b>ai_addr</b> member in each returned 
<b>addrinfoW</b> structure points to a filled-in socket address structure, the length of which is specified in its <b>ai_addrlen</b> member.

If the <i>pNodeName</i> parameter points to a computer name, all permanent addresses for the computer that can be used as a source address are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="https://msdn.microsoft.com/bdafc4a4-5f3c-4dd5-ba9b-4f6045a82652">GetUnicastIpAddressTable</a> or <a href="https://msdn.microsoft.com/d5475c09-05dd-41d7-80ff-63c52d78468c">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to false in the <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure. 

If the <i>pNodeName</i> parameter points to a string equal to "localhost", all loopback addresses on the local computer are returned. 

If the <i>pNodeName</i> parameter contains an empty string, all registered addresses on the local computer are returned. 

On Windows Server 2003 and later if the <i>pNodeName</i> parameter points to a string equal to "..localmachine", all registered addresses on the local computer are returned. 

If the <i>pNodeName</i> parameter refers to a cluster virtual server name, only virtual server addresses are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="https://msdn.microsoft.com/bdafc4a4-5f3c-4dd5-ba9b-4f6045a82652">GetUnicastIpAddressTable</a> or <a href="https://msdn.microsoft.com/d5475c09-05dd-41d7-80ff-63c52d78468c">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to true in the <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure. See <a href="https://msdn.microsoft.com/47247d48-d401-41dc-9aae-128840eb6d3a">Windows Clustering</a> for more information about clustering.

Windows 7 with Service Pack 1 (SP1) and Windows Server 2008 R2 with Service Pack 1 (SP1) add support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This also changes the behavior such that if the <b>SkipAsSource</b> member in the <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  

A hotfix is available for Windows 7 and Windows Server 2008 R2 that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address.  This hotfix also changes behavior such that if the <b>SkipAsSource</b> member in the <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  For more information, see <a href=" http://go.microsoft.com/fwlink/p/?linkid=208218">Knowledge Base (KB) 2386184</a>.   

A similar hotfix is also available for Windows Vista with Service Pack 2 (SP2) and Windows Server 2008 with Service Pack 2 (SP2) that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This hotfix also changes behavior such that if the <b>SkipAsSource</b> member in the <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=208219">Knowledge Base (KB) 975808</a>. 


Callers of the 
<b>GetAddrInfoW</b> function can provide hints about the type of socket supported through an 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure pointed to by the <i>pHints</i> parameter. When the <i>pHints</i> parameter is used, the following rules apply to its associated 
<b>addrinfoW</b> structure:

<ul>
<li>A value of <b>AF_UNSPEC</b> for <b>ai_family</b> indicates the caller will accept only the <b>AF_INET</b> and <b>AF_INET6</b> address families. Note that <b>AF_UNSPEC</b> and <b>PF_UNSPEC</b> are the same.</li>
<li>A value of zero for <b>ai_socktype</b> indicates the caller will accept any socket type.</li>
<li>A value of zero for <b>ai_protocol</b> indicates the caller will accept any protocol.</li>
<li>The <b>ai_addrlen</b> member must be set to zero.</li>
<li>The <b>ai_canonname</b> member must be set to <b>NULL</b>.</li>
<li>The <b>ai_addr</b> member must be set to <b>NULL</b>.</li>
<li>The <b>ai_next</b> member must be set to <b>NULL</b>.</li>
</ul>


Other values in the 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure provided in the <i>pHints</i> parameter indicate specific requirements. For example, if the caller handles only IPv4 and does not handle IPv6, the <b>ai_family</b> member should be set to <b>AF_INET</b>. For another example, if the caller handles only TCP and does not handle UDP, the <b>ai_socktype</b> member should be set to <b>SOCK_STREAM</b>.

If the <i>pHints</i> parameter is a <b>NULL</b> pointer, the 
<b>GetAddrInfoW</b> function handles it as if the 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure in <i>pHints</i> were initialized with its <b>ai_family</b> member set to <b>AF_UNSPEC</b> and all other members set to zero.

On Windows Vista and later when <b>GetAddrInfoW</b> is called from a service, if the operation is the result of a user process calling the service, then the service should impersonate the user.  This is to allow security to be properly enforced.

The 
<b>GetAddrInfoW</b> function can be used to convert a text string representation of an IP address to an <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>structure that contains a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure for the IP address and other information. To be used in this way, the string pointed to by the <i>pNodeName</i> parameter must contain a text representation of an IP address and the <b>addrinfoW</b>structure pointed to by the <i>pHints</i> parameter must have the <b>AI_NUMERICHOST</b> flag set in the <b>ai_flags</b> member. The string pointed to by the <i>pNodeName</i> parameter may contain a text representation of either an IPv4 or an IPv6 address. The text IP address is converted to an <b>addrinfoW</b>structure pointed to by the <i>ppResult</i> parameter. The returned <b>addrinfoW</b>structure contains a <b>sockaddr</b> structure for the IP address along with additional information about the IP address. For this method to work with an IPv6 address string on Windows Server 2003 and Windows XP, the IPv6 protocol must be installed on the local computer. Otherwise, the <a href="windows_sockets_error_codes_2.htm">WSAHOST_NOT_FOUND</a> error is returned.

<h3><a id="Freeing_Address_Information_from_Dynamic_Allocation"></a><a id="freeing_address_information_from_dynamic_allocation"></a><a id="FREEING_ADDRESS_INFORMATION_FROM_DYNAMIC_ALLOCATION"></a>Freeing Address Information from Dynamic Allocation</h3>
All information returned by the 
<b>GetAddrInfoW</b> function pointed to by the <i>ppResult</i> parameter is dynamically allocated, including all 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structures, socket address structures, and canonical host name strings pointed to by 
<b>addrinfoW</b> structures. Memory allocated by a successful call to this function must be released with a subsequent call to <a href="https://msdn.microsoft.com/0a2a226c-2068-4538-b499-04cfbfd65b8a">FreeAddrInfoW</a>.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following code example shows how to use the <b>GetAddrInfoW</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include &lt;winsock2.h&gt;
#include &lt;Ws2tcpip.h&gt;
#include &lt;stdio.h&gt;

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

// set APPVER=5.02 for WinXP SP2 and later

int __cdecl wmain(int argc, wchar_t **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;
    INT iRetval;

    DWORD dwRetval;

    int i = 1;
    
    ADDRINFOW *result = NULL;
    ADDRINFOW *ptr = NULL;
    ADDRINFOW hints;

//    struct sockaddr_in6 *sockaddr_ipv6;
    LPSOCKADDR sockaddr_ip;

    wchar_t ipstringbuffer[46];
    DWORD ipbufferlength = 46;

    // Validate the parameters
    if (argc != 3) {
        wprintf(L"usage: %ws &lt;hostname&gt; &lt;servicename&gt;\n", argv[0]);
        wprintf(L"getaddrinfow provides protocol-independent translation\n");
        wprintf(L"   from an Unicode host name to an IP address\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws www.contoso.com 0\n", argv[0]);
        return 1;
    }


    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }

    //--------------------------------
    // Setup the hints address info structure
    // which is passed to the getaddrinfo() function
    ZeroMemory( &amp;hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    wprintf(L"Calling getaddrinfow with following parameters:\n");
    wprintf(L"\tnodename = %ws\n", argv[1]);
    wprintf(L"\tservname (or port) = %ws\n\n", argv[2]);
    

//--------------------------------
// Call GetAddrinfoW(). If the call succeeds,
// the result variable will hold a linked list
// of addrinfow structures containing response
// information
    dwRetval = GetAddrInfoW(argv[1], argv[2], &amp;hints, &amp;result);
    if ( dwRetval != 0 ) {
        wprintf(L"GetAddrInfoW failed with error: %d\n", dwRetval);
        WSACleanup();
        return 1;
    }

    wprintf(L"GetAddrInfoW returned success\n");
    
    // Retrieve each address and print out the hex bytes
    for(ptr=result; ptr != NULL ;ptr=ptr-&gt;ai_next) {

        wprintf(L"GetAddrInfoW response %d\n", i++);
        wprintf(L"\tFlags: 0x%x\n", ptr-&gt;ai_flags);
        wprintf(L"\tFamily: ");
        switch (ptr-&gt;ai_family) {
            case AF_UNSPEC:
                wprintf(L"Unspecified\n");
                break;
            case AF_INET:
                wprintf(L"AF_INET (IPv4)\n");
                sockaddr_ip = (LPSOCKADDR) ptr-&gt;ai_addr;
                // The buffer length is changed by each call to WSAAddresstoString
                // So we need to set it for each iteration through the loop for safety
                ipbufferlength = 46;
                iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr-&gt;ai_addrlen, NULL, 
                    ipstringbuffer, &amp;ipbufferlength );
                if (iRetval)
                    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
                else    
                    wprintf(L"\tIPv4 address %ws\n", ipstringbuffer);
                break;
            case AF_INET6:
                wprintf(L"AF_INET6 (IPv6)\n");
                // the InetNtop function is available on Windows Vista and later
                // sockaddr_ipv6 = (struct sockaddr_in6 *) ptr-&gt;ai_addr;
                // printf("\tIPv6 address %s\n",
                //    InetNtop(AF_INET6, &amp;sockaddr_ipv6-&gt;sin6_addr, ipstringbuffer, 46) );
                
                // We use WSAAddressToString since it is supported on Windows XP and later
                sockaddr_ip = (LPSOCKADDR) ptr-&gt;ai_addr;
                // The buffer length is changed by each call to WSAAddresstoString
                // So we need to set it for each iteration through the loop for safety
                ipbufferlength = 46;
                iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr-&gt;ai_addrlen, NULL, 
                    ipstringbuffer, &amp;ipbufferlength );
                if (iRetval)
                    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
                else    
                    wprintf(L"\tIPv6 address %ws\n", ipstringbuffer);
                break;
            default:
                wprintf(L"Other %ld\n", ptr-&gt;ai_family);
                break;
        }
        wprintf(L"\tSocket type: ");
        switch (ptr-&gt;ai_socktype) {
            case 0:
                wprintf(L"Unspecified\n");
                break;
            case SOCK_STREAM:
                wprintf(L"SOCK_STREAM (stream)\n");
                break;
            case SOCK_DGRAM:
                wprintf(L"SOCK_DGRAM (datagram) \n");
                break;
            case SOCK_RAW:
                wprintf(L"SOCK_RAW (raw) \n");
                break;
            case SOCK_RDM:
                wprintf(L"SOCK_RDM (reliable message datagram)\n");
                break;
            case SOCK_SEQPACKET:
                wprintf(L"SOCK_SEQPACKET (pseudo-stream packet)\n");
                break;
            default:
                wprintf(L"Other %ld\n", ptr-&gt;ai_socktype);
                break;
        }
        wprintf(L"\tProtocol: ");
        switch (ptr-&gt;ai_protocol) {
            case 0:
                wprintf(L"Unspecified\n");
                break;
            case IPPROTO_TCP:
                wprintf(L"IPPROTO_TCP (TCP)\n");
                break;
            case IPPROTO_UDP:
                wprintf(L"IPPROTO_UDP (UDP) \n");
                break;
            default:
                wprintf(L"Other %ld\n", ptr-&gt;ai_protocol);
                break;
        }
        wprintf(L"\tLength of this sockaddr: %d\n", ptr-&gt;ai_addrlen);
        wprintf(L"\tCanonical name: %s\n", ptr-&gt;ai_canonname);
    }

    FreeAddrInfoW(result);
    WSACleanup();

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>

<div class="alert"><b>Note</b>  Ensure that the development environment targets the newest version of <i>Ws2tcpip.h</i> which includes structure and function definitions for <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> and <b>GetAddrInfoW</b>, respectively.</div>
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
   IDNs in a standard fashion.  The specifications for IDNs and IDNA are documented in <a href="http://go.microsoft.com/fwlink/p/?LinkID=390166">RFC 3490</a>, <a href="http://go.microsoft.com/fwlink/p/?LinkID=390167">RTF 5890</a>, and <a href="http://go.microsoft.com/fwlink/p/?LinkID=390169">RFC 6365</a> published by the Internet Engineering Task Force (IETF).


On Windows 8 and Windows Server 2012, the <b>GetAddrInfoW</b> function provides support for Internationalized Domain Name (IDN) parsing applied to the name passed in the <i>pNodeName</i> parameter. Winsock performs Punycode/IDN encoding and conversion.  This behavior can be disabled using the <b>AI_DISABLE_IDN_ENCODING</b> flag discussed below.

On Windows 7 and Windows Server 2008 R2 or earlier, the <b>GetAddrInfoW</b> function does not currently provide support for IDN parsing applied to the name passed in the <i>pNodeName</i> parameter. Winsock does not perform any Punycode/IDN conversion.  The <b>GetAddrInfoW</b> function does not use Punycode to convert an IDN as per <a href="http://go.microsoft.com/fwlink/p/?LinkID=390166">RFC 3490</a>. The <b>GetAddrInfoW</b> function when querying DNS encodes the Unicode name in UTF-8 format, the format used by Microsoft DNS servers in an enterprise environment.

Several functions on Windows Vista and later support conversion between Unicode labels in an IDN to their ASCII equivalents. The resulting representation of each  Unicode label contains only ASCII characters and starts with the xn-- prefix if the Unicode label contained any non-ASCII characters. The reason for this is to support existing DNS servers on the Internet, since some DNS tools and servers only support ASCII characters (see <a href="http://go.microsoft.com/fwlink/p/?LinkID=390166">RFC 3490</a>). 

 

The <a href="https://msdn.microsoft.com/e39aa5c2-3f76-40b2-9948-bbd795c6c525">IdnToAscii</a> function use Punycode to convert an IDN to the ASCII representation of the original Unicode string using the standard algorithm defined in <a href="http://go.microsoft.com/fwlink/p/?LinkID=390166">RFC 3490</a>. The <a href="https://msdn.microsoft.com/90707414-aef7-4265-bc2b-d48ac79db099">IdnToUnicode</a> function converts the ASCII form of an IDN to the normal Unicode UTF-16 encoding syntax. For more information and links to related draft standards, see <a href="_win32_IDN">Handling Internationalized Domain Names (IDNs)</a>.



The <a href="https://msdn.microsoft.com/e39aa5c2-3f76-40b2-9948-bbd795c6c525">IdnToAscii</a> function can be used to convert an IDN name to the ASCII form. To pass this ASCII form to the  <b>GetAddrInfoW</b> function, you can use the <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> function to convert the <b>CHAR</b> string into a <b>WCHAR</b> string that then can be passed in the <i>pNodeName</i> parameter to the <b>GetAddrInfoW</b> function. 

<h3><a id="ai_flags"></a><a id="AI_FLAGS"></a>Use of ai_flags in the hints parameter</h3>


Flags in the <b>ai_flags</b> member of the optional 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure provided in the <i>pHints</i> parameter modify the behavior of the function. 

These flag bits are defined in the <i>Ws2def.h</i> header file on the Microsoft Windows Software Development Kit (SDK) for Windows 7. These flag bits are defined in the <i>Ws2tcpip.h</i> header file on the Windows SDK for Windows Server 2008 and Windows Vista.  These flag bits are defined in the <i>Ws2tcpip.h</i> header file on the Platform Software Development Kit (SDK) for   Windows Server 2003, and Windows XP. 

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
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function. When the <b>AI_PASSIVE</b> flag is set and <i>pNodeName</i> is a <b>NULL</b> pointer, the IP address portion of the socket address structure is set to <b>INADDR_ANY</b> for IPv4 addresses and <b>IN6ADDR_ANY_INIT</b> for IPv6 addresses.

When the <b>AI_PASSIVE</b> flag is not set, the returned socket address structure is ready for a call to the 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> function for a connection-oriented protocol, or ready for a call to either the 
<b>connect</b>, 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>, or 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> functions for a connectionless protocol. If the <i>pNodeName</i> parameter is a <b>NULL</b> pointer in this case, the IP address portion of the socket address structure is set to the loopback address.

</td>
</tr>
<tr>
<td width="40%">
<a id="AI_CANONNAME"></a><a id="ai_canonname"></a><b>AI_CANONNAME</b>

</td>
<td width="60%">
If neither <b>AI_CANONNAME</b> nor <b>AI_NUMERICHOST</b> is used, the 
<b>GetAddrInfoW</b> function attempts resolution. If a literal string is passed 
<b>GetAddrInfoW</b> attempts to convert the string, and if a host name is passed the 
<b>GetAddrInfoW</b> function attempts to resolve the name to an address or multiple addresses.

When the <b>AI_CANONNAME</b> bit is set, the <i>pNodeName</i> parameter cannot be <b>NULL</b>. Otherwise the 
<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function will  fail with <a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a>.

When the <b>AI_CANONNAME</b> bit is set and the 
<b>GetAddrInfoW</b> function returns success, the <b>ai_canonname</b> member in the <i>ppResult</i> parameter points to a <b>NULL</b>-terminated string that contains the canonical name of the specified node.

<div class="alert"><b>Note</b>  The <b>GetAddrInfoW</b> function can return success when the <b>AI_CANONNAME</b> flag is set, yet the <b>ai_canonname</b> member in the associated 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure is <b>NULL</b>. Therefore, the recommended use of the <b>AI_CANONNAME</b> flag includes testing whether the <b>ai_canonname</b> member in the associated 
<b>addrinfoW</b> structure is <b>NULL</b>.</div>
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
If the <b>AI_ADDRCONFIG</b> bit is set, <b>GetAddrInfoW</b> will resolve only if a global address is configured. If <b>AI_ADDRCONFIG</b> flag is specified, IPv4 addresses shall be
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
If the  <b>AI_FQDN</b> is set and a flat name (single label) is specified,  <b>GetAddrInfoW</b> will return the fully qualified domain name that the name eventually resolved to. The fully qualified domain name is returned in the <b>ai_canonname</b> member in the associated 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure. This is different than <b>AI_CANONNAME</b> bit flag that returns the canonical name registered in DNS which may be different than the fully qualified domain name  that the flat name resolved to. Only one of the <b>AI_FQDN</b> and <b>AI_CANONNAME</b> bits can be set. The <b>GetAddrInfoW</b> function will fail if both flags are present with <b>EAI_BADFLAGS</b>.


When the <b>AI_FQDN</b> bit is set, the <i>pNodeName</i> parameter cannot be <b>NULL</b>. Otherwise the 
<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function will  fail with <a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a>.

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
<tr>
<td width="40%">
<a id="AI_DISABLE_IDN_ENCODING"></a><a id="ai_disable_idn_encoding"></a><b>AI_DISABLE_IDN_ENCODING</b>

</td>
<td width="60%">
If the  <b>AI_DISABLE_IDN_ENCODING</b> is set, this disables the automatic International Domain Name encoding using Punycode in the name resolution functions called by the <b>GetAddrInfoW</b> function. 

<b>Windows 8:  </b>The <b>AI_DISABLE_IDN_ENCODING</b> flag is defined on the Windows SDK for  Windows 8 and later.    The <b>AI_DISABLE_IDN_ENCODING</b> flag is supported on Windows 8 and later. 

</td>
</tr>
</table>
 



<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/0a2a226c-2068-4538-b499-04cfbfd65b8a">FreeAddrInfoW</a>



<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/787EB209-5944-4F0A-8550-FE1115C2298A">GetHostNameW</a>



<a href="https://msdn.microsoft.com/e39aa5c2-3f76-40b2-9948-bbd795c6c525">IdnToAscii</a>



<a href="https://msdn.microsoft.com/90707414-aef7-4265-bc2b-d48ac79db099">IdnToUnicode</a>



<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>



<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a>



<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>



<a href="https://msdn.microsoft.com/1077e03d-a1a4-45ab-a5d2-29a67e03f5df">addrinfoex</a>



<a href="https://msdn.microsoft.com/9CB33347-A838-473D-B5CD-1149D6632CF2">addrinfoex2</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/00b4c5de-89c9-419f-bff8-822ef0446697">gai_strerror</a>



<a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>



<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>



<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

