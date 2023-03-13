---
UID: NS:wininet.INTERNET_PROXY_INFO
title: INTERNET_PROXY_INFO (wininet.h)
description: Contains information that is supplied with the INTERNET_OPTION_PROXY value to get or set proxy information on a handle obtained from a call to the InternetOpen function.
helpviewer_keywords: ["*LPINTERNET_PROXY_INFO","INTERNET_OPEN_TYPE_DIRECT","INTERNET_OPEN_TYPE_PRECONFIG","INTERNET_OPEN_TYPE_PROXY","INTERNET_PROXY_INFO","INTERNET_PROXY_INFO structure [WinINet]","LPINTERNET_PROXY_INFO","LPINTERNET_PROXY_INFO structure pointer [WinINet]","_inet_internet_proxy_info_structure","wininet.internet_proxy_info","wininet/ LPINTERNET_PROXY_INFO","wininet/INTERNET_PROXY_INFO"]
old-location: wininet\internet_proxy_info.htm
tech.root: wininet
ms.assetid: f2431800-dbcc-4933-87f5-2d08ca22ad9c
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_PROXY_INFO, INTERNET_OPEN_TYPE_DIRECT, INTERNET_OPEN_TYPE_PRECONFIG, INTERNET_OPEN_TYPE_PROXY, INTERNET_PROXY_INFO, INTERNET_PROXY_INFO structure [WinINet], LPINTERNET_PROXY_INFO, LPINTERNET_PROXY_INFO structure pointer [WinINet], _inet_internet_proxy_info_structure, wininet.internet_proxy_info, wininet/ LPINTERNET_PROXY_INFO, wininet/INTERNET_PROXY_INFO'
req.header: wininet.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERNET_PROXY_INFO, *LPINTERNET_PROXY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPINTERNET_PROXY_INFO
 - wininet/LPINTERNET_PROXY_INFO
 - INTERNET_PROXY_INFO
 - wininet/INTERNET_PROXY_INFO
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
 - INTERNET_PROXY_INFO
---

# INTERNET_PROXY_INFO structure


## -description

Contains information that is supplied with the INTERNET_OPTION_PROXY value to get or set proxy information on a handle obtained from a call to the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopena">InternetOpen</a> function.

## -struct-fields

### -field dwAccessType

Access type. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_OPEN_TYPE_DIRECT"></a><a id="internet_open_type_direct"></a><dl>
<dt><b>INTERNET_OPEN_TYPE_DIRECT</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed through a direct connection. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_OPEN_TYPE_PRECONFIG"></a><a id="internet_open_type_preconfig"></a><dl>
<dt><b>INTERNET_OPEN_TYPE_PRECONFIG</b></dt>
</dl>
</td>
<td width="60%">
Applies only when setting proxy information. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_OPEN_TYPE_PROXY"></a><a id="internet_open_type_proxy"></a><dl>
<dt><b>INTERNET_OPEN_TYPE_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed using a proxy. 

</td>
</tr>
</table>

### -field lpszProxy

Pointer to a string that contains the proxy server list.

### -field lpszProxyBypass

Pointer to a string that contains the proxy bypass list.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a>

