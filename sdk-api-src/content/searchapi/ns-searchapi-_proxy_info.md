---
UID: NS:searchapi._PROXY_INFO
title: "_PROXY_INFO"
author: windows-driver-content
description: Stores information about a proxy. Used by ISearchProtocol.
old-location: search\_search_PROXY_INFO.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\proxy_info.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PROXY_INFO, PROXY_INFO structure [search], _PROXY_INFO, _search_PROXY_INFO, search._search_PROXY_INFO, searchapi/PROXY_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PROXY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	PROXY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _PROXY_INFO structure


## -description


Stores information about a proxy. Used by <a href="https://msdn.microsoft.com/f11ff5a5-d03c-4cb8-970c-78345d204492">ISearchProtocol</a>.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of the structure in bytes.


### -field pcwszUserAgent

Type: <b>LPCWSTR</b>

A pointer to a Unicode string buffer containing the user agent string.


### -field paUseProxy

Type: <b><a href="https://msdn.microsoft.com/40104593-80f1-4ac5-811c-b923b1a72435">PROXY_ACCESS</a></b>

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

