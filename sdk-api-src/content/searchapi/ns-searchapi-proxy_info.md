---
UID: NS:searchapi._PROXY_INFO
title: PROXY_INFO (searchapi.h)
description: Stores information about a proxy. Used by ISearchProtocol.
helpviewer_keywords: ["PROXY_INFO","PROXY_INFO structure [search]","_search_PROXY_INFO","search._search_PROXY_INFO","searchapi/PROXY_INFO"]
old-location: search\_search_PROXY_INFO.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\proxy_info.htm
ms.date: 12/05/2018
ms.keywords: PROXY_INFO, PROXY_INFO structure [search], _search_PROXY_INFO, search._search_PROXY_INFO, searchapi/PROXY_INFO
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROXY_INFO
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _PROXY_INFO
 - searchapi/_PROXY_INFO
 - PROXY_INFO
 - searchapi/PROXY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - PROXY_INFO
---

# PROXY_INFO structure


## -description

Stores information about a proxy. Used by <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol">ISearchProtocol</a>.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size of the structure in bytes.

### -field pcwszUserAgent

Type: <b>LPCWSTR</b>

A pointer to a Unicode string buffer containing the user agent string.

### -field paUseProxy

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-proxy_access">PROXY_ACCESS</a></b>

The proxy type to use.

### -field fLocalBypass

Type: <b>BOOL</b>

The bypass proxy for local addresses.

### -field dwPortNumber

Type: <b>DWORD</b>

The port number to use.

### -field pcwszProxyName

Type: <b>LPCWSTR</b>

A pointer to a Unicode string buffer that contains the name of the proxy server.

### -field pcwszBypassList

Type: <b>LPCWSTR</b>

The list of sites that will bypass the proxy.