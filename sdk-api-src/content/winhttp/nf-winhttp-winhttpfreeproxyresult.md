---
UID: NF:winhttp.WinHttpFreeProxyResult
title: WinHttpFreeProxyResult function (winhttp.h)
description: The WinHttpFreeProxyResult function frees the data retrieved from a previous call to WinHttpGetProxyResult.
helpviewer_keywords: ["WinHttpFreeProxyResult","WinHttpFreeProxyResult function [WinHTTP]","http.winhttpfreeproxyresult","winhttp/WinHttpFreeProxyResult"]
old-location: http\winhttpfreeproxyresult.htm
tech.root: http
ms.assetid: 0484bf54-066f-4a7f-8d1a-079eb4b001bd
ms.date: 12/05/2018
ms.keywords: WinHttpFreeProxyResult, WinHttpFreeProxyResult function [WinHTTP], http.winhttpfreeproxyresult, winhttp/WinHttpFreeProxyResult
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHttpFreeProxyResult
 - winhttp/WinHttpFreeProxyResult
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
 - WinHttpFreeProxyResult
---

## -description

Frees the data retrieved from a previous call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyresult">WinHttpGetProxyResult</a>.

## -parameters

### -param pProxyResult [in, out]

A pointer to a <a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result">WINHTTP_PROXY_RESULT</a> structure retrieved from a previous call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyresult">WinHttpGetProxyResult</a>.

## -returns

This function does not return a value.

## -remarks

Upon completion, all internal members of <i>pProxyResult</i> will be zeroed and the memory allocated to those members will be freed. If <i>pProxyResult</i> is an allocated pointer, the caller must free the pointer.