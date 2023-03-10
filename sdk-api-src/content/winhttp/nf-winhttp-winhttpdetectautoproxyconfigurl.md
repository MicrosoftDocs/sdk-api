---
UID: NF:winhttp.WinHttpDetectAutoProxyConfigUrl
title: WinHttpDetectAutoProxyConfigUrl function (winhttp.h)
description: Finds the URL for the Proxy Auto-Configuration (PAC) file.
helpviewer_keywords: ["WINHTTP_AUTO_DETECT_TYPE_DHCP","WINHTTP_AUTO_DETECT_TYPE_DNS_A","WinHttpDetectAutoProxyConfigUrl","WinHttpDetectAutoProxyConfigUrl function [WinHTTP]","http.winhttpdetectautoproxyconfigurl","winhttp/WinHttpDetectAutoProxyConfigUrl"]
old-location: http\winhttpdetectautoproxyconfigurl.htm
tech.root: http
ms.assetid: a433ed3c-3f31-4c37-9c09-3f8344e9550d
ms.date: 12/05/2018
ms.keywords: WINHTTP_AUTO_DETECT_TYPE_DHCP, WINHTTP_AUTO_DETECT_TYPE_DNS_A, WinHttpDetectAutoProxyConfigUrl, WinHttpDetectAutoProxyConfigUrl function [WinHTTP], http.winhttpdetectautoproxyconfigurl, winhttp/WinHttpDetectAutoProxyConfigUrl
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHttpDetectAutoProxyConfigUrl
 - winhttp/WinHttpDetectAutoProxyConfigUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpDetectAutoProxyConfigUrl
---

# WinHttpDetectAutoProxyConfigUrl function


## -description

The <b>WinHttpDetectAutoProxyConfigUrl</b> function finds the URL for the Proxy Auto-Configuration (PAC) file. This function reports the URL of the PAC file, but it does not download the file.

## -parameters

### -param dwAutoDetectFlags [in]

A data type that specifies what protocols to use to locate the PAC file. If both the DHCP and DNS auto detect flags are set, DHCP is used first; if no PAC URL is discovered using DHCP, then DNS is used.

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

### -param ppwstrAutoConfigUrl [out]

 A data type that returns a pointer to a null-terminated Unicode string that contains the configuration URL that receives the proxy data. You must free the string pointed to by <i>ppwszAutoConfigUrl</i> using the <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_AUTODETECTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Returned if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

WinHTTP implements the <a href="https://www.ietf.org/archive/id/draft-ietf-wrec-wpad-01.txt">Web Proxy Auto-Discovery (WPAD) protocol</a>, often referred to as <i>autoproxy</i>. For more information about well-known locations, see the  <a href="https://www.ietf.org/archive/id/draft-ietf-wrec-wpad-01.txt">Discovery Process</a> section of the WPAD protocol document.

Note that because the <b>WinHttpDetectAutoProxyConfigUrl</b> function takes time to complete its operation, it should not be called from  a UI thread.

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>