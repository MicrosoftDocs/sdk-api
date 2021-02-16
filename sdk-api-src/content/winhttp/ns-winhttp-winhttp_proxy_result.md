---
UID: NS:winhttp._WINHTTP_PROXY_RESULT
title: WINHTTP_PROXY_RESULT (winhttp.h)
description: The WINHTTP_PROXY_RESULT structure contains collection of proxy result entries provided by WinHttpGetProxyResult.
helpviewer_keywords: ["WINHTTP_PROXY_RESULT","WINHTTP_PROXY_RESULT structure [HTTP]","http.winhttp_proxy_result","winhttp/WINHTTP_PROXY_RESULT"]
old-location: http\winhttp_proxy_result.htm
tech.root: http
ms.assetid: 6a621701-3325-4877-99ba-8580ad07739d
ms.date: 12/05/2018
ms.keywords: WINHTTP_PROXY_RESULT, WINHTTP_PROXY_RESULT structure [HTTP], http.winhttp_proxy_result, winhttp/WINHTTP_PROXY_RESULT
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
req.typenames: WINHTTP_PROXY_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_PROXY_RESULT
 - winhttp/_WINHTTP_PROXY_RESULT
 - WINHTTP_PROXY_RESULT
 - winhttp/WINHTTP_PROXY_RESULT
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
 - WINHTTP_PROXY_RESULT
---

# WINHTTP_PROXY_RESULT structure


## -description

The <b>WINHTTP_PROXY_RESULT</b> structure contains  collection of proxy result entries provided by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyresult">WinHttpGetProxyResult</a>.

## -struct-fields

### -field cEntries

The number of entries in the <b>pEntries</b> array.

### -field pEntries

A pointer to an array of <a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry">WINHTTP_PROXY_RESULT_ENTRY</a> structures.

## -see-also

<a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry">WINHTTP_PROXY_RESULT_ENTRY</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpfreeproxyresult">WinHttpFreeProxyResult</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyresult">WinHttpGetProxyResult</a>