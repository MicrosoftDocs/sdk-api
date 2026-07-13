---
UID: NF:windns.DnsQueryConfig
title: DnsQueryConfig function (windns.h)
description: The DnsQueryConfig function enables application programmers to query for the configuration of the local computer or a specific adapter.
helpviewer_keywords: ["DnsQueryConfig","DnsQueryConfig function [DNS]","_dns_dnsqueryconfig","dns.dnsqueryconfig","windns/DnsQueryConfig"]
old-location: dns\dnsqueryconfig.htm
tech.root: DNS
ms.assetid: 83de7df8-7e89-42fe-b609-1dc173afc9df
ms.date: 12/05/2018
ms.keywords: DnsQueryConfig, DnsQueryConfig function [DNS], _dns_dnsqueryconfig, dns.dnsqueryconfig, windns/DnsQueryConfig
req.header: windns.h
req.include-header: 
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsQueryConfig
 - windns/DnsQueryConfig
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
 - DnsQueryConfig
---

# DnsQueryConfig function


## -description

The 
<b>DnsQueryConfig</b> function enables application programmers to query for the configuration of the local computer or a specific adapter.

## -parameters

### -param Config [in]

A <a href="/windows/win32/api/windns/ne-windns-dns_config_type">DNS_CONFIG_TYPE</a> value that specifies the configuration type of the information to be queried.

### -param Flag [in]

A value that specifies whether to allocate memory for the configuration information. Set <i>Flag</i> to <b>DNS_CONFIG_FLAG_ALLOC </b> to allocate memory; otherwise, set it to 0.  

<div class="alert"><b>Note</b>  Free the allocated memory with <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.</div>
<div> </div>

### -param pwsAdapterName [in, optional]

A pointer to a string that represents the adapter name against which the query is run.

### -param pReserved [in, optional]

Reserved for future use.

### -param pBuffer [out]

A pointer to a buffer that receives the query response. The following table shows the data type of the buffer for each  of the <i>Config</i> parameter values.

<table>
<tr>
<th><i>Config</i> parameter</th>
<th>Data type of buffer</th>
</tr>
<tr>
<td>DnsConfigPrimaryDomainName_W</td>
<td>PWCHAR</td>
</tr>
<tr>
<td>DnsConfigPrimaryDomainName_A</td>
<td>PCHAR</td>
</tr>
<tr>
<td>DnsConfigPrimaryDomainName_UTF8</td>
<td>PCHAR</td>
</tr>
<tr>
<td>DnsConfigAdapterDomainName_W</td>
<td>Not implemented</td>
</tr>
<tr>
<td>DnsConfigAdapterDomainName_A</td>
<td>Not implemented</td>
</tr>
<tr>
<td>DnsConfigAdapterDomainName_UTF8</td>
<td>Not implemented</td>
</tr>
<tr>
<td>DnsConfigDnsServerList</td>
<td>IP4_ARRAY</td>
</tr>
<tr>
<td>DnsConfigSearchList</td>
<td>Not implemented</td>
</tr>
<tr>
<td>DnsConfigAdapterInfo</td>
<td>Not implemented</td>
</tr>
<tr>
<td>DnsConfigPrimaryHostNameRegistrationEnabled</td>
<td>DWORD</td>
</tr>
<tr>
<td>DnsConfigAdapterHostNameRegistrationEnabled</td>
<td>DWORD</td>
</tr>
<tr>
<td>DnsConfigAddressRegistrationMaxCount</td>
<td>DWORD</td>
</tr>
<tr>
<td>DnsConfigHostName_W</td>
<td>PWCHAR</td>
</tr>
<tr>
<td>DnsConfigHostName_A</td>
<td>PCHAR</td>
</tr>
<tr>
<td>DnsConfigHostName_UTF8</td>
<td>PCHAR</td>
</tr>
<tr>
<td>DnsConfigFullHostName_W</td>
<td>PWCHAR</td>
</tr>
<tr>
<td>DnsConfigFullHostName_A</td>
<td>PCHAR</td>
</tr>
<tr>
<td>DnsConfigFullHostName_UTF8</td>
<td>PCHAR</td>
</tr>
</table>

### -param pBufLen [in, out]

The length of the buffer, in bytes. If the buffer provided is not sufficient, an error is returned and <i>pBufferLength</i> contains the minimum necessary buffer size. Ignored on input if <i>Flag</i> is set to <b>TRUE</b>.

## -returns

Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.

## -see-also

<a href="/windows/win32/api/windns/ne-windns-dns_config_type">DNS_CONFIG_TYPE</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>