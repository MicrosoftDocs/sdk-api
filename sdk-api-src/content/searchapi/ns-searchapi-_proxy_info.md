---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

