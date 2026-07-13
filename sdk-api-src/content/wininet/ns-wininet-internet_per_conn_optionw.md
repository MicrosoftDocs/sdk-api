---
UID: NS:wininet.INTERNET_PER_CONN_OPTIONW
title: INTERNET_PER_CONN_OPTIONW (wininet.h)
description: Contains the value of an option. (Unicode)
helpviewer_keywords: ["*LPINTERNET_PER_CONN_OPTIONW","INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_TIME","INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_URL","INTERNET_PER_CONN_AUTOCONFIG_RELOAD_DELAY_MINS","INTERNET_PER_CONN_AUTOCONFIG_SECONDARY_URL","INTERNET_PER_CONN_AUTOCONFIG_URL","INTERNET_PER_CONN_AUTODISCOVERY_FLAGS","INTERNET_PER_CONN_FLAGS","INTERNET_PER_CONN_FLAGS_UI","INTERNET_PER_CONN_OPTION","INTERNET_PER_CONN_OPTION structure [WinINet]","INTERNET_PER_CONN_OPTIONA","INTERNET_PER_CONN_OPTIONW","INTERNET_PER_CONN_PROXY_BYPASS","INTERNET_PER_CONN_PROXY_SERVER","LPINTERNET_PER_CONN_OPTION","LPINTERNET_PER_CONN_OPTION structure pointer [WinINet]","_inet_internet_per_conn_option_structure","wininet.internet_per_conn_option","wininet/INTERNET_PER_CONN_OPTION","wininet/INTERNET_PER_CONN_OPTIONA","wininet/INTERNET_PER_CONN_OPTIONW","wininet/LPINTERNET_PER_CONN_OPTION"]
old-location: wininet\internet_per_conn_option.htm
tech.root: wininet
ms.assetid: 35cfc768-1f1d-4be9-8d56-c56c7440513e
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_PER_CONN_OPTIONW, INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_TIME, INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_URL, INTERNET_PER_CONN_AUTOCONFIG_RELOAD_DELAY_MINS, INTERNET_PER_CONN_AUTOCONFIG_SECONDARY_URL, INTERNET_PER_CONN_AUTOCONFIG_URL, INTERNET_PER_CONN_AUTODISCOVERY_FLAGS, INTERNET_PER_CONN_FLAGS, INTERNET_PER_CONN_FLAGS_UI, INTERNET_PER_CONN_OPTION, INTERNET_PER_CONN_OPTION structure [WinINet], INTERNET_PER_CONN_OPTIONA, INTERNET_PER_CONN_OPTIONW, INTERNET_PER_CONN_PROXY_BYPASS, INTERNET_PER_CONN_PROXY_SERVER, LPINTERNET_PER_CONN_OPTION, LPINTERNET_PER_CONN_OPTION structure pointer [WinINet], _inet_internet_per_conn_option_structure, wininet.internet_per_conn_option, wininet/INTERNET_PER_CONN_OPTION, wininet/INTERNET_PER_CONN_OPTIONA, wininet/INTERNET_PER_CONN_OPTIONW, wininet/LPINTERNET_PER_CONN_OPTION'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INTERNET_PER_CONN_OPTIONW (Unicode) and INTERNET_PER_CONN_OPTIONA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERNET_PER_CONN_OPTIONW, *LPINTERNET_PER_CONN_OPTIONW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPINTERNET_PER_CONN_OPTIONW
 - wininet/LPINTERNET_PER_CONN_OPTIONW
 - INTERNET_PER_CONN_OPTIONW
 - wininet/INTERNET_PER_CONN_OPTIONW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_PER_CONN_OPTION
 - INTERNET_PER_CONN_OPTIONA
 - INTERNET_PER_CONN_OPTIONW
---

# INTERNET_PER_CONN_OPTIONW structure


## -description

Contains the value of an option.

## -struct-fields

### -field dwOption

Option to be queried or set. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_AUTOCONFIG_URL"></a><a id="internet_per_conn_autoconfig_url"></a><dl>
<dt><b>INTERNET_PER_CONN_AUTOCONFIG_URL</b></dt>
</dl>
</td>
<td width="60%">
Sets or retrieves a string containing the URL to the automatic configuration script. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_AUTODISCOVERY_FLAGS"></a><a id="internet_per_conn_autodiscovery_flags"></a><dl>
<dt><b>INTERNET_PER_CONN_AUTODISCOVERY_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the automatic discovery settings. The 
<b>Value</b> member will contain one or more of the following values: 

<dl>
<dt>AUTO_PROXY_FLAG_ALWAYS_DETECT</dt>
<dd>
Always automatically detect settings. 

</dd>
<dt>AUTO_PROXY_FLAG_CACHE_INIT_RUN</dt>
<dd>
Indicates that the cached results of the automatic proxy configuration script should be used, instead of actually running the script, unless the cached file has expired. 

</dd>
<dt>AUTO_PROXY_FLAG_DETECTION_RUN</dt>
<dd>
Automatic detection has been run at least once on this connection. 

</dd>
<dt>AUTO_PROXY_FLAG_DETECTION_SUSPECT</dt>
<dd>
Not currently supported. 

</dd>
<dt>AUTO_PROXY_FLAG_DONT_CACHE_PROXY_RESULT</dt>
<dd>
Do not allow the caching of the result of the automatic proxy configuration script. 

</dd>
<dt>AUTO_PROXY_FLAG_MIGRATED</dt>
<dd>
The setting was migrated from a Microsoft Internet Explorer 4.0 installation, and automatic detection should be attempted once. 

</dd>
<dt>AUTO_PROXY_FLAG_USER_SET</dt>
<dd>
The user has explicitly set the automatic detection. 

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_FLAGS"></a><a id="internet_per_conn_flags"></a><dl>
<dt><b>INTERNET_PER_CONN_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the connection type. The 
<b>Value</b> member will contain one or more of the following values: 

<dl>
<dt>PROXY_TYPE_DIRECT</dt>
<dd>
The connection does not use a proxy server. 

</dd>
<dt>PROXY_TYPE_PROXY</dt>
<dd>
The connection uses an explicitly set proxy server. 

</dd>
<dt>PROXY_TYPE_AUTO_PROXY_URL</dt>
<dd>
The connection downloads and processes an automatic configuration script at a specified URL. 

</dd>
<dt>PROXY_TYPE_AUTO_DETECT</dt>
<dd>
The connection automatically detects settings. 

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_PROXY_BYPASS"></a><a id="internet_per_conn_proxy_bypass"></a><dl>
<dt><b>INTERNET_PER_CONN_PROXY_BYPASS</b></dt>
</dl>
</td>
<td width="60%">
Sets or retrieves a string containing the URLs that do not use the proxy server. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_PROXY_SERVER"></a><a id="internet_per_conn_proxy_server"></a><dl>
<dt><b>INTERNET_PER_CONN_PROXY_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Sets or retrieves a string containing the proxy servers. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_AUTOCONFIG_SECONDARY_URL"></a><a id="internet_per_conn_autoconfig_secondary_url"></a><dl>
<dt><b>INTERNET_PER_CONN_AUTOCONFIG_SECONDARY_URL</b></dt>
</dl>
</td>
<td width="60%">
Chained autoconfig URL. Used when the primary autoconfig URL points to an INS file that sets a second autoconfig URL for proxy information. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_AUTOCONFIG_RELOAD_DELAY_MINS"></a><a id="internet_per_conn_autoconfig_reload_delay_mins"></a><dl>
<dt><b>INTERNET_PER_CONN_AUTOCONFIG_RELOAD_DELAY_MINS</b></dt>
</dl>
</td>
<td width="60%">
of minutes until automatic refresh of autoconfig URL by autodiscovery. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_TIME"></a><a id="internet_per_conn_autoconfig_last_detect_time"></a><dl>
<dt><b>INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_TIME</b></dt>
</dl>
</td>
<td width="60%">
Read only option. Returns the time the last known good autoconfig URL was found using autodiscovery. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_URL"></a><a id="internet_per_conn_autoconfig_last_detect_url"></a><dl>
<dt><b>INTERNET_PER_CONN_AUTOCONFIG_LAST_DETECT_URL</b></dt>
</dl>
</td>
<td width="60%">
Read only option. Returns the last known good URL found using autodiscovery. 

</td>
</tr>
</table>
 



<b>Windows 7 and later:  </b><p class="note">Clients that support Internet Explorer 8 should query the connection type using <b>INTERNET_PER_CONN_FLAGS_UI</b>.  If this query fails, then the system is running a previous version of Internet Explorer and the client should query again with  <b>INTERNET_PER_CONN_FLAGS</b>.

<p class="note">Restore the connection type using   <b>INTERNET_PER_CONN_FLAGS</b> regardless of the version of Internet Explorer.







<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_PER_CONN_FLAGS_UI"></a><a id="internet_per_conn_flags_ui"></a><dl>
<dt><b>INTERNET_PER_CONN_FLAGS_UI</b></dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the connection type. The 
<b>Value</b> member will contain one or more of the following values: 

<dl>
<dt>PROXY_TYPE_DIRECT</dt>
<dd>
The connection does not use a proxy server. 

</dd>
<dt>PROXY_TYPE_PROXY</dt>
<dd>
The connection uses an explicitly set proxy server. 

</dd>
<dt>PROXY_TYPE_AUTO_PROXY_URL</dt>
<dd>
The connection downloads and processes an automatic configuration script at a specified URL. 

</dd>
<dt>PROXY_TYPE_AUTO_DETECT</dt>
<dd>
The connection automatically detects settings. 

</dd>
</dl>
</td>
</tr>
</table>

### -field Value

Union that contains the value for the option. It can be any one of the following types depending on the value of 
<b>dwOption</b>:



#### dwValue

Unsigned long integer value.



#### pszValue

Pointer to a string value.



#### ftValue

A 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

### -field dwValue

### -field pszValue

### -field ftValue

 




##### - Value.dwValue

Unsigned long integer value.


##### - Value.ftValue

A 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.


##### - Value.pszValue

Pointer to a string value.

## -remarks

In Internet Explorer 5, only the ANSI versions of 
<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a> and 
<a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a> will work with the 
<b>INTERNET_PER_CONN_OPTION</b> structure. The Unicode versions will support the 
<b>INTERNET_PER_CONN_OPTION</b> structure in later versions of Internet Explorer.

For queries that return strings, 
<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a> allocates the memory for the 
<b>pszValue</b> member of the structure. The calling application must free this memory using the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function when it has finished using the string.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines INTERNET_PER_CONN_OPTION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/ns-wininet-internet_per_conn_option_lista">INTERNET_PER_CONN_OPTION_LIST</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a>

