---
UID: NS:winhttp._WINHTTP_PROXY_INFO
title: WINHTTP_PROXY_INFO (winhttp.h)
description: The WINHTTP_PROXY_INFO structure contains the session or default proxy configuration.
helpviewer_keywords: ["*LPWINHTTP_PROXY_INFO","WINHTTP_ACCESS_TYPE_DEFAULT_PROXY","WINHTTP_ACCESS_TYPE_NAMED_PROXY","WINHTTP_ACCESS_TYPE_NO_PROXY","WINHTTP_PROXY_INFO","WINHTTP_PROXY_INFO structure [HTTP]","WINHTTP_PROXY_INFOW","http.internet_proxy_info","winhttp/WINHTTP_PROXY_INFO","winhttp_internet_proxy_info_structure"]
old-location: http\internet_proxy_info.htm
tech.root: http
ms.assetid: acb51bc5-43e2-4657-96eb-8e3d3e82e018
ms.date: 12/05/2018
ms.keywords: '*LPWINHTTP_PROXY_INFO, WINHTTP_ACCESS_TYPE_DEFAULT_PROXY, WINHTTP_ACCESS_TYPE_NAMED_PROXY, WINHTTP_ACCESS_TYPE_NO_PROXY, WINHTTP_PROXY_INFO, WINHTTP_PROXY_INFO structure [HTTP], WINHTTP_PROXY_INFOW, http.internet_proxy_info, winhttp/WINHTTP_PROXY_INFO, winhttp_internet_proxy_info_structure'
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINHTTP_PROXY_INFO, *LPWINHTTP_PROXY_INFO
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - LPWINHTTP_PROXY_INFO
 - winhttp/LPWINHTTP_PROXY_INFO
 - WINHTTP_PROXY_INFO
 - winhttp/WINHTTP_PROXY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_PROXY_INFO
---

## -description

The <b>WINHTTP_PROXY_INFO</b> structure contains the session or default proxy configuration.

## -struct-fields

### -field dwAccessType

Unsigned long integer value that contains the access type. This can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_NO_PROXY"></a><a id="winhttp_access_type_no_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_NO_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed through a direct connection. 

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_DEFAULT_PROXY"></a><a id="winhttp_access_type_default_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Applies only when setting proxy information. 

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_NAMED_PROXY"></a><a id="winhttp_access_type_named_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed using a proxy. 

</td>
</tr>
</table>

### -field lpszProxy

Pointer to a string value that contains the proxy server list.

### -field lpszProxyBypass

Pointer to a string value that contains the proxy bypass list.

## -remarks

This structure is used with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> and 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> to get or set the proxy configuration for the current session by specifying the WINHTTP_OPTION_PROXY flag.

This structure is used with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration">WinHttpSetDefaultProxyConfiguration</a> and 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration">WinHttpGetDefaultProxyConfiguration</a> to get or set the default proxy configuration in the registry.

The proxy server list contains one or more of the following strings separated by semicolons or whitespace.



``` syntax
([<scheme>=][<scheme>"://"]<server>[":"<port>])
```

The proxy bypass list contains one or more server names separated by semicolons or whitespace.  The proxy bypass list can also contain the string "&lt;local&gt;" to indicate that all local intranet sites are bypassed.  Local intranet sites are considered to be all servers that do not contain a period in their name.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP
		  Versions</a>
