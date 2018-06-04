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

# DnsQueryConfig function


## -description



			The 
<b>DnsQueryConfig</b> function enables application programmers to query for the configuration of the local computer or a specific adapter.


## -parameters




### -param Config [in]

A <a href="https://msdn.microsoft.com/e0f0cc05-dcfe-48df-8dbd-e756cfa69154">DNS_CONFIG_TYPE</a> value that specifies the configuration type of the information to be queried.


### -param Flag [in]

A value that specifies whether to allocate memory for the configuration information. Set <i>Flag</i> to <b>DNS_CONFIG_FLAG_ALLOC </b> to allocate memory; otherwise, set it to 0.  

<div class="alert"><b>Note</b>  Free the allocated memory with <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.</div>
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
 


### -param pBufLen

TBD




#### - pBufferLength [in, out]

The length of the buffer, in bytes. If the buffer provided is not sufficient, an error is returned and <i>pBufferLength</i> contains the minimum necessary buffer size. Ignored on input if <i>Flag</i> is set to <b>TRUE</b>.


## -returns




						Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/e0f0cc05-dcfe-48df-8dbd-e756cfa69154">DNS_CONFIG_TYPE</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>
 

 

