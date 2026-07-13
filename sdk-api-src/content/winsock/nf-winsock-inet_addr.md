---
UID: NF:winsock.inet_addr
title: inet_addr function (winsock.h)
description: The inet_addr function (winsock.h) converts a string containing an IPv4 dotted-decimal address into a proper address for the IN_ADDR structure.
helpviewer_keywords: ["_win32_inet_addr_2","inet_addr","inet_addr function [Winsock]","winsock.inet_addr_2","wsipv6ok/inet_addr"]
old-location: winsock\inet_addr_2.htm
tech.root: WinSock
ms.assetid: 7d6df658-9d83-45c7-97e7-b2a016a73847
ms.date: 08/15/2022
ms.keywords: _win32_inet_addr_2, inet_addr, inet_addr function [Winsock], winsock.inet_addr_2, wsipv6ok/inet_addr
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
 - inet_addr
 - winsock/inet_addr
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
 - inet_addr
---

# inet_addr function


## -description

The 
<b>inet_addr</b> function converts a string containing an IPv4 dotted-decimal address into a proper address for the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure.

## -parameters

### -param cp

TBD




#### - a [in]

A <b>NULL</b>-terminated character string representing a number expressed in the Internet standard ".'' (dotted) notation.

## -returns

If no error occurs, 
the <b>inet_addr</b> function returns an unsigned long value containing a suitable binary representation of the Internet address given. 

If the string in the <i>cp</i> parameter does not contain a legitimate Internet address, for example if a portion of an "a.b.c.d" address exceeds 255, then 
<b>inet_addr</b> returns the value <b>INADDR_NONE</b>.

On Windows Server 2003 and later if the string in the <i>cp</i> parameter is an empty string, then 
<b>inet_addr</b> returns the value <b>INADDR_NONE</b>.  If <b>NULL</b> is passed in the <i>cp</i> parameter, then 
<b>inet_addr</b> returns the value <b>INADDR_NONE</b>.

On Windows XP and earlier if the string in the <i>cp</i> parameter is an empty string, then 
<b>inet_addr</b> returns the value <b>INADDR_ANY</b>. If <b>NULL</b> is passed in the <i>cp</i> parameter, then 
<b>inet_addr</b> returns the value <b>INADDR_NONE</b>.

## -remarks

The 
<b>inet_addr</b> function interprets the character string specified by the <i>cp</i> parameter. This string represents a numeric Internet address expressed in the Internet standard ".'' notation. The value returned is a number suitable for use as an Internet address. All Internet addresses are returned in IP's network order (bytes ordered from left to right). If you pass in " " (a space) to the 
<b>inet_addr</b> function, 
<b>inet_addr</b> returns zero.

On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a> function can be used to convert a string representation of an IPv4 address to a binary IPv4 address represented as an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure. On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a> function can be used to convert a string representation of an IPv6 address to a binary IPv6 address represented as an <b>IN6_ADDR</b> structure. 

<h3><a id="Internet_Addresses"></a><a id="internet_addresses"></a><a id="INTERNET_ADDRESSES"></a>Internet Addresses</h3>
Values specified using the ".'' notation take one of the following forms:

a.b.c.d a.b.c a.b a

When four parts are specified, each is interpreted as a byte of data and assigned, from left to right, to the 4 bytes of an Internet address. When an Internet address is viewed as a 32-bit integer quantity on the Intel architecture, the bytes referred to above appear as "d.c.b.a''. That is, the bytes on an Intel processor are ordered from right to left.

The parts that make up an address in "." notation can be decimal, octal or hexadecimal as specified in the C language. Numbers that start with "0x" or "0X" imply hexadecimal. Numbers that start with "0" imply octal. All other numbers are interpreted as decimal.

<table>
<tr>
<th>Internet address value</th>
<th>Meaning</th>
</tr>
<tr>
<td>"4.3.2.16"</td>
<td>Decimal</td>
</tr>
<tr>
<td>"004.003.002.020"</td>
<td>Octal</td>
</tr>
<tr>
<td>"0x4.0x3.0x2.0x10"</td>
<td>Hexadecimal</td>
</tr>
<tr>
<td>"4.003.002.0x10"</td>
<td>Mix</td>
</tr>
</table>
 

The <b>inet_addr</b> function supports the decimal, octal, hexadecimal, and mixed notations for the string passed in the <i>cp</i> parameter.

<div class="alert"><b>Note</b>  The following notations are only used by Berkeley software, and nowhere else on the Internet. For compatibility with Berkeley software, the <b>inet_addr</b> function also supports the additional notations specified below. </div>
<div> </div>
When a three-part address is specified, the last part is interpreted as a 16-bit quantity and placed in the right-most 2 bytes of the network address. This makes the three-part address format convenient for specifying Class B network addresses as "128.net.host''

When a two-part address is specified, the last part is interpreted as a 24-bit quantity and placed in the right-most 3 bytes of the network address. This makes the two-part address format convenient for specifying Class A network addresses as "net.host''.

When only one part is given, the value is stored directly in the network address without any byte rearrangement.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

The following code example shows how to use the <b>inet_addr</b> function.


```cpp
#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <stdio.h>
#include <windows.h>


// need link with Ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int __cdecl main(int argc, char **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    unsigned long ulAddr = INADDR_NONE;

    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s <IPv4 address>\n", argv[0]);
        printf("  inetaddr converts a string containing an\n");
        printf("  IPv4 address in one of the supported formats\n");
        printf("  to a unsigned long representing an IN_ADDR\n");
        printf("      %s 192.168.16.34\n", argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

//--------------------------------
// Call inet_addr(). If the call succeeds,
// the result variable will hold a IN_ADDR
    ulAddr = inet_addr(argv[1]);
    if ( ulAddr == INADDR_NONE ) {
        printf("inet_addr failed and returned INADDR_NONE\n");
        WSACleanup();
        return 1;
    }   
    
    if (ulAddr == INADDR_ANY) {
        printf("inet_addr failed and returned INADDR_ANY\n");
        WSACleanup();
        return 1;  
    }

    printf("inet_addr returned success\n");
    
    // Here we could implement code to retrieve each address and 
    // print out the hex bytes
    // for(i=0, ptr= (Char*) &ulAddr; i < 4; i++, ptr++) {

    WSACleanup();
    return 0;
}

```

## -see-also

<b>IN6_ADDR</b>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>
