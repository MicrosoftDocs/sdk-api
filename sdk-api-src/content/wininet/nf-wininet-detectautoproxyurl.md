---
UID: NF:wininet.DetectAutoProxyUrl
title: DetectAutoProxyUrl function (wininet.h)
description: The DetectAutoProxyUrl function (wininet.h) attempts to determine the location of a WPAD autoproxy script.
helpviewer_keywords: ["DetectAutoProxyUrl","DetectAutoProxyUrl function [WinINet]","PROXY_AUTO_DETECT_TYPE_DHCP","PROXY_AUTO_DETECT_TYPE_DNS_A","_inet_detectautoproxyurl_function","wininet.detectautoproxyurl","winineti/DetectAutoProxyUrl"]
old-location: wininet\detectautoproxyurl.htm
tech.root: wininet
ms.assetid: 4e94ab0c-0f39-4e6e-a272-6beff61e97c6
ms.date: 08/10/2022
ms.keywords: DetectAutoProxyUrl, DetectAutoProxyUrl function [WinINet], PROXY_AUTO_DETECT_TYPE_DHCP, PROXY_AUTO_DETECT_TYPE_DNS_A, _inet_detectautoproxyurl_function, wininet.detectautoproxyurl, winineti/DetectAutoProxyUrl
req.header: wininet.h
req.include-header: Wininet.h
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DetectAutoProxyUrl
 - wininet/DetectAutoProxyUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - DetectAutoProxyUrl
---

# DetectAutoProxyUrl function


## -description

Attempts to determine the location of a WPAD autoproxy script.

## -parameters

### -param pszAutoProxyUrl [in, out]

Pointer to a buffer to receive the URL from which a WPAD autoproxy script can be downloaded.

### -param cchAutoProxyUrl [in]

Size of 
the buffer pointed to by <i>lpszAutoProxyUrl</i>, in bytes.

### -param dwDetectFlags [in]

Automation detection type. This parameter can be one or both of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROXY_AUTO_DETECT_TYPE_DHCP"></a><a id="proxy_auto_detect_type_dhcp"></a><dl>
<dt><b>PROXY_AUTO_DETECT_TYPE_DHCP</b></dt>
</dl>
</td>
<td width="60%">
Use a Dynamic Host Configuration Protocol (DHCP) search to identify the proxy.

</td>
</tr>
<tr>
<td width="40%"><a id="PROXY_AUTO_DETECT_TYPE_DNS_A"></a><a id="proxy_auto_detect_type_dns_a"></a><dl>
<dt><b>PROXY_AUTO_DETECT_TYPE_DNS_A</b></dt>
</dl>
</td>
<td width="60%">
Use a well qualified name search to identify the proxy.

</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa384580(v=vs.85)">InternetDeInitializeAutoProxyDll</a>



<a href="/windows/desktop/WinInet/internetgetproxyinfo">InternetGetProxyInfo</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a>
