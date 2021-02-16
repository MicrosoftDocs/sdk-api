---
UID: NS:winhttp._WINHTTP_PROXY_RESULT_ENTRY
title: WINHTTP_PROXY_RESULT_ENTRY (winhttp.h)
description: The WINHTTP_PROXY_RESULT_ENTRY structure contains a result entry from a call to WinHttpGetProxyResult.
helpviewer_keywords: ["WINHTTP_PROXY_RESULT_ENTRY","WINHTTP_PROXY_RESULT_ENTRY structure [HTTP]","http.winhttp_proxy_result_entry","winhttp/WINHTTP_PROXY_RESULT_ENTRY"]
old-location: http\winhttp_proxy_result_entry.htm
tech.root: http
ms.assetid: d1652b34-67a9-40ad-a495-836147e5cc88
ms.date: 12/05/2018
ms.keywords: WINHTTP_PROXY_RESULT_ENTRY, WINHTTP_PROXY_RESULT_ENTRY structure [HTTP], http.winhttp_proxy_result_entry, winhttp/WINHTTP_PROXY_RESULT_ENTRY
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WINHTTP_PROXY_RESULT_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_PROXY_RESULT_ENTRY
 - winhttp/_WINHTTP_PROXY_RESULT_ENTRY
 - WINHTTP_PROXY_RESULT_ENTRY
 - winhttp/WINHTTP_PROXY_RESULT_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_PROXY_RESULT_ENTRY
---

# WINHTTP_PROXY_RESULT_ENTRY structure


## -description

The <b>WINHTTP_PROXY_RESULT_ENTRY</b> structure contains a result entry from a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyresult">WinHttpGetProxyResult</a>.

## -struct-fields

### -field fProxy

A <b>BOOL</b> that whether a result is from a proxy. It is set to <b>TRUE</b>   if the result contains a proxy or <b>FALSE</b> if the result does not contain a proxy.

### -field fBypass

A BOOL that indicates if the result is bypassing a proxy (on an intranet). It is set to  <b>TRUE</b> if the result is bypassing a proxy or <b>FALSE</b> if all traffic is direct. This parameter applies only if <i>fProxy</i> is <b>FALSE</b>.

### -field ProxyScheme

An <a href="/windows/desktop/WinHttp/internet-scheme">INTERNET_SCHEME</a> value that specifies the scheme of the proxy.

### -field pwszProxy

A string that contains the hostname of the proxy.

### -field ProxyPort

An <a href="/windows/desktop/WinHttp/internet-port">INTERNET_PORT</a> value that specifies the port of the proxy.

## -remarks

This structure is stored in an array inside of a <a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result">WINHTTP_PROXY_RESULT</a> structure.

## -see-also

<a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result">WINHTTP_PROXY_RESULT</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpfreeproxyresult">WinHttpFreeProxyResult</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyresult">WinHttpGetProxyResult</a>