---
UID: NF:windns.DnsValidateServerStatus
title: DnsValidateServerStatus function (windns.h)
description: The DnsValidateServerStatus function validates an IP address as a suitable DNS server.
helpviewer_keywords: ["DNS_VALSVR_ERROR_INVALID_ADDR","DNS_VALSVR_ERROR_INVALID_NAME","DNS_VALSVR_ERROR_NO_AUTH","DNS_VALSVR_ERROR_NO_RESPONSE","DNS_VALSVR_ERROR_NO_TCP","DNS_VALSVR_ERROR_REFUSED","DNS_VALSVR_ERROR_UNKNOWN","DNS_VALSVR_ERROR_UNREACHABLE","DnsValidateServerStatus","DnsValidateServerStatus function [DNS]","ERROR_SUCCESS","dns.dnsvalidateserverstatus","windns/DnsValidateServerStatus"]
old-location: dns\dnsvalidateserverstatus.htm
tech.root: DNS
ms.assetid: 5b362d05-87b2-44dd-8198-bcb5ab5a64f6
ms.date: 12/05/2018
ms.keywords: DNS_VALSVR_ERROR_INVALID_ADDR, DNS_VALSVR_ERROR_INVALID_NAME, DNS_VALSVR_ERROR_NO_AUTH, DNS_VALSVR_ERROR_NO_RESPONSE, DNS_VALSVR_ERROR_NO_TCP, DNS_VALSVR_ERROR_REFUSED, DNS_VALSVR_ERROR_UNKNOWN, DNS_VALSVR_ERROR_UNREACHABLE, DnsValidateServerStatus, DnsValidateServerStatus function [DNS], ERROR_SUCCESS, dns.dnsvalidateserverstatus, windns/DnsValidateServerStatus
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsValidateServerStatus
 - windns/DnsValidateServerStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsValidateServerStatus
---

# DnsValidateServerStatus function


## -description

The 
<b>DnsValidateServerStatus</b> function validates an IP address as a suitable DNS server.

## -parameters

### -param server [in]

A pointer to a <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> that contains the DNS server IPv4 or IPv6  address to be examined.

### -param queryName [in]

                A pointer to a Unicode string that represents the fully qualified domain name (FQDN) of the owner of the record set that is queried.

### -param serverStatus [out]

                A pointer to a DWORD that represents the query validation status.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ERROR_SUCCESS"></a><a id="error_success"></a><dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
No errors. The call was successful.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_INVALID_ADDR"></a><a id="dns_valsvr_error_invalid_addr"></a><dl>
<dt><b>DNS_VALSVR_ERROR_INVALID_ADDR</b></dt>
</dl>
</td>
<td width="60%">
<i>server</i> IP address was invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_INVALID_NAME"></a><a id="dns_valsvr_error_invalid_name"></a><dl>
<dt><b>DNS_VALSVR_ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
<i>queryName</i> FQDN was invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_UNREACHABLE"></a><a id="dns_valsvr_error_unreachable"></a><dl>
<dt><b>DNS_VALSVR_ERROR_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
DNS server was unreachable.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_NO_RESPONSE"></a><a id="dns_valsvr_error_no_response"></a><dl>
<dt><b>DNS_VALSVR_ERROR_NO_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Timeout waiting for the DNS server response.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_NO_AUTH"></a><a id="dns_valsvr_error_no_auth"></a><dl>
<dt><b>DNS_VALSVR_ERROR_NO_AUTH</b></dt>
</dl>
</td>
<td width="60%">
DNS server was not authoritative or <i>queryName</i> was not found.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_REFUSED"></a><a id="dns_valsvr_error_refused"></a><dl>
<dt><b>DNS_VALSVR_ERROR_REFUSED</b></dt>
</dl>
</td>
<td width="60%">
DNS server refused the query.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_NO_TCP"></a><a id="dns_valsvr_error_no_tcp"></a><dl>
<dt><b>DNS_VALSVR_ERROR_NO_TCP</b></dt>
</dl>
</td>
<td width="60%">
The TCP query did not return ERROR_SUCCESS after the validation system had already completed a successful query to the DNS server using UDP.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_VALSVR_ERROR_UNKNOWN"></a><a id="dns_valsvr_error_unknown"></a><dl>
<dt><b>DNS_VALSVR_ERROR_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
An unknown error occurred.

</td>
</tr>
</table>

## -returns

The 
<b>DnsValidateServerStatus</b> function has the following possible return values:

## -see-also

<a href="/windows/desktop/DNS/dns-functions">DNS Functions</a>