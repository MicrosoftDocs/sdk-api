---
UID: NF:ip2string.RtlIpv4AddressToStringExA
tech.root: IpHlp 
title: RtlIpv4AddressToStringExA
ms.date: 04/14/2021
targetos: Windows
description: Converts an IPv4 address and port number to a string in Internet standard format. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Ntdll.dll 
req.header: ip2string.h
req.idl: 
req.include-header: Mstcpip.h 
req.irql: 
req.kmdf-ver: 
req.lib: ntdll.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps] 
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlIpv4AddressToStringExA
 - RtlIpv4AddressToStringEx
f1_keywords:
 - RtlIpv4AddressToStringExA
 - ip2string/RtlIpv4AddressToStringExA
 - RtlIpv4AddressToStringEx
 - ip2string/RtlIpv4AddressToStringEx
dev_langs:
 - c++
---

# RtlIpv4AddressToStringExA function

## -description

The <b>RtlIpv4AddressToStringEx</b> function  converts an IPv4 address and port number to a string in Internet standard format.

## -parameters

### -param Address [in]

The IPv4 address in network byte order.

### -param Port [in]

The port number in network byte order format. This parameter is optional.

### -param AddressString [out]

A pointer to the buffer to receive the <b>NULL</b>-terminated string representation of the IPv4 address and port. This buffer should be large enough to hold at least INET_ADDRSTRLEN characters. The INET_ADDRSTRLEN value is defined in the <i>Ws2ipdef.h</i> header file.

### -param AddressStringLength [in, out]

On input, the number of characters that fit in the buffer pointed to by the <i>AddressString</i> parameter, including the NULL terminator.

On output, this parameter contains the number of characters actually written to the buffer pointed to by the <i>AddressString</i> parameter.

## -returns

If the function succeeds, the return value is <b>STATUS_SUCCESS</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>AddressString</i> or <i>AddressStringLength</i> parameter. This error is also returned if the length of the buffer pointed to by the <i>AddressString</i> parameter is not large enough to receive the string representation of the IPv4 address and port.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.
</td>
</tr>
</table>

## -remarks

The <b>RtlIpv4AddressToStringEx</b> function is used to convert an IPv4 address and port number to the string representation of the IPv4 address in Internet dotted-decimal format followed by a colon character and a string representation of the port.

<b>RtlIpv4AddressToStringEx</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform IP address to string conversion.

If the length of the buffer pointed to by the <i>AddressString</i> parameter is not large enough to receive the string representation of the IPv4 address and port, <b>RtlIpv4AddressToStringEx</b> returns <b>ERROR_INVALID_PARAMETER</b> and sets the <i>AddressStringLength</i> parameter to the buffer length required.

When either UNICODE or _UNICODE is defined, <b>RtlIpv4AddressToStringEx</b> is defined to <b>RtlIpv4AddressToStringExW</b>, the Unicode version of this function. The <i>AddressString</i> parameter is defined to the PWSTR data type.

When both UNICODE and _UNICODE are not defined, <b>RtlIpv4AddressToStringEx</b> is defined to <b>RtlIpv4AddressToStringExA</b>, the ANSI version of this function. The <i>AddressString</i> parameter is defined to the PSTR data type.

The <b>IN_ADDR</b> structure is defined in the <i>Inaddr.h</i> header file.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>  
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>  
<a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-inet_ntop">InetNtop</a>  
<a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-inet_pton">InetPton</a>  
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexa">RtlIpv4StringToAddressEx</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexa">RtlIpv6AddressToStringEx</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexa">RtlIpv6StringToAddressEx</a>  
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>  
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>  
