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

# WINHTTP_AUTOPROXY_OPTIONS structure


## -description


The <b>WINHTTP_AUTOPROXY_OPTIONS</b> structure is used to indicate to the <a href="https://msdn.microsoft.com/d01b101e-a496-4e84-9aec-61afe3920fbb">WinHttpGetProxyForURL</a> function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.


## -struct-fields




### -field dwFlags

Mechanisms should be used to obtain the PAC file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_AUTO_DETECT"></a><a id="winhttp_autoproxy_auto_detect"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_AUTO_DETECT</b></dt>
</dl>
</td>
<td width="60%">
Attempt to automatically discover the URL of the PAC file using both DHCP and DNS queries to the local network.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_CONFIG_URL"></a><a id="winhttp_autoproxy_config_url"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_CONFIG_URL</b></dt>
</dl>
</td>
<td width="60%">
Download the PAC file from the URL specified by <b>lpszAutoConfigUrl</b> in the <b>WINHTTP_AUTOPROXY_OPTIONS</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_NO_CACHE_CLIENT_"></a><a id="winhttp_autoproxy_no_cache_client_"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_NO_CACHE_CLIENT </b></dt>
</dl>
</td>
<td width="60%">
Disables querying a host to proxy cache of script execution results in the current process.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_NO_CACHE_SVC"></a><a id="winhttp_autoproxy_no_cache_svc"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_NO_CACHE_SVC</b></dt>
</dl>
</td>
<td width="60%">
Disables querying a host to proxy cache of script execution results in the autoproxy service.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_NO_DIRECTACCESS"></a><a id="winhttp_autoproxy_no_directaccess"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_NO_DIRECTACCESS</b></dt>
</dl>
</td>
<td width="60%">
Disables querying Direct Access proxy settings for this request.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_RUN_INPROCESS"></a><a id="winhttp_autoproxy_run_inprocess"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_RUN_INPROCESS</b></dt>
</dl>
</td>
<td width="60%">
Executes the Web Proxy Auto-Discovery (WPAD) protocol in-process instead of delegating to an out-of-process WinHTTP AutoProxy Service, if available. This flag must be combined with one of the other flags.

This option has no effect when passed to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_RUN_OUTPROCESS_ONLY"></a><a id="winhttp_autoproxy_run_outprocess_only"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_RUN_OUTPROCESS_ONLY</b></dt>
</dl>
</td>
<td width="60%">
By default,  WinHTTP is configured to fall back to auto-discover a proxy in-process. If this fallback behavior is undesirable in the event that an out-of-process discovery  fails,  it can be  disabled using  this flag.

This option has no effect when passed to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.


<div class="alert"><b>Note</b>  This flag is available on Windows Server 2003 only.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTOPROXY_SORT_RESULTS_"></a><a id="winhttp_autoproxy_sort_results_"></a><dl>
<dt><b>WINHTTP_AUTOPROXY_SORT_RESULTS </b></dt>
</dl>
</td>
<td width="60%">
Orders the proxy results based on a heuristic placing the fastest proxies first.

</td>
</tr>
</table>
 


### -field dwAutoDetectFlags

If <b>dwFlags</b> includes the WINHTTP_AUTOPROXY_AUTO_DETECT flag, then <b>dwAutoDetectFlags</b> specifies what protocols are to be used to locate the PAC file. If both the DHCP and DNS auto detect flags are specified, then DHCP is used first; if no PAC URL is discovered using DHCP, then DNS is used.

If <b>dwFlags</b> does not include the WINHTTP_AUTOPROXY_AUTO_DETECT flag, then <b>dwAutoDetectFlags</b> must be zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTO_DETECT_TYPE_DHCP"></a><a id="winhttp_auto_detect_type_dhcp"></a><dl>
<dt><b>WINHTTP_AUTO_DETECT_TYPE_DHCP</b></dt>
</dl>
</td>
<td width="60%">
Use DHCP to locate the proxy auto-configuration file.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTO_DETECT_TYPE_DNS_A"></a><a id="winhttp_auto_detect_type_dns_a"></a><dl>
<dt><b>WINHTTP_AUTO_DETECT_TYPE_DNS_A</b></dt>
</dl>
</td>
<td width="60%">
Use DNS to attempt to locate the proxy auto-configuration file at a well-known location on the domain of the local computer.

</td>
</tr>
</table>
 


### -field lpszAutoConfigUrl

If <b>dwFlags</b> includes the WINHTTP_AUTOPROXY_CONFIG_URL flag, the <b>lpszAutoConfigUrl</b> must point to a <b>null</b>-terminated Unicode string that contains the URL of the proxy auto-configuration (PAC) file.

If <b>dwFlags</b> does not include the WINHTTP_AUTOPROXY_CONFIG_URL flag, then <b>lpszAutoConfigUrl</b> must be <b>NULL</b>.


### -field lpvReserved

Reserved for future use; must be <b>NULL</b>.


### -field dwReserved

Reserved for future use; must be zero.


### -field fAutoLogonIfChallenged

Specifies whether the client's domain credentials should be automatically sent in response to an NTLM or Negotiate Authentication challenge when WinHTTP requests the PAC file.

If this flag is TRUE, credentials should automatically be sent in response to an authentication challenge. If this flag is FALSE and authentication is required to download the PAC file, the <a href="https://msdn.microsoft.com/d01b101e-a496-4e84-9aec-61afe3920fbb">WinHttpGetProxyForUrl</a> function fails.


## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP
		  Versions</a>
 

 

