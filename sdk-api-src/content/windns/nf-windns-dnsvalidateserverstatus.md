---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DnsValidateServerStatus function


## -description


The 
<b>DnsValidateServerStatus</b> function validates an IP address as a suitable DNS server. 


## -parameters




### -param server [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a> that contains the DNS server IPv4 or IPv6  address to be examined.


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
<td width="40%"><a id="_DNS_VALSVR_ERROR_INVALID_NAME"></a><a id="_dns_valsvr_error_invalid_name"></a><dl>
<dt><b>
DNS_VALSVR_ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
<i>queryName</i> FQDN was invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="_DNS_VALSVR_ERROR_UNREACHABLE"></a><a id="_dns_valsvr_error_unreachable"></a><dl>
<dt><b>
DNS_VALSVR_ERROR_UNREACHABLE</b></dt>
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




<a href="https://msdn.microsoft.com/9b3c1c20-5516-41de-b00f-b95736ff53f1">DNS Functions</a>
 

 

