---
UID: NF:winineti.CreateUrlCacheContainerW
title: CreateUrlCacheContainerW function
author: windows-sdk-content
description: Creates a cache container in the specified cache path to hold cache entries based on the specified name, cache prefix, and container type.
old-location: wininet\createurlcachecontainer.htm
tech.root: wininet
ms.assetid: 19b518cc-2f02-49c3-bedc-f5d633cc635d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreateUrlCacheContainer, CreateUrlCacheContainer function [WinINet], CreateUrlCacheContainerA, CreateUrlCacheContainerW, wininet.createurlcachecontainer, winineti/CreateUrlCacheContainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winineti.h
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - CreateUrlCacheContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateUrlCacheContainerW function


## -description


Creates a cache container in the specified cache path to hold cache entries based on the specified name, cache prefix, and container type.
<div class="alert"><b>Note</b>  Note: This API is deprecated. Please use the <a href="https://msdn.microsoft.com/library/gg269259">Extensible Storage Engine</a> instead.</div><div> </div>

## -parameters




### -param Name [in]

The name to give to the cache.


### -param lpCachePrefix [in]

The cache prefix to base the cache on.


### -param lpszCachePath [in, optional]

The cache prefix to create the cache in.


### -param KBCacheLimit [in]

The size limit of the cache in whole kilobytes, or 0 for the default size.


### -param dwContainerType [in]

The container type to base the cache on.


### -param dwOptions [in]

This parameter is reserved and must be 0.


### -param pvBuffer

This parameter is reserved and must be <b>NULL</b>.


### -param cbBuffer [in, out]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/0124e664-85a3-4637-9d91-7ec23025a87b">CommitUrlCacheEntry</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

