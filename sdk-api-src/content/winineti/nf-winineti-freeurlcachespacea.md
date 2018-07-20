---
UID: NF:winineti.FreeUrlCacheSpaceA
title: FreeUrlCacheSpaceA function
author: windows-sdk-content
description: Clears the space in the specified URL cache.
old-location: wininet\freeurlcachespace.htm
old-project: wininet
ms.assetid: 5853CA64-551F-484E-A992-25B9EA6C74C2
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FreeUrlCacheSpace, FreeUrlCacheSpace function [WinINet], FreeUrlCacheSpaceA, FreeUrlCacheSpaceW, wininet.freeurlcachespace, winineti/FreeUrlCacheSpace, winineti/FreeUrlCacheSpaceA, winineti/FreeUrlCacheSpaceW
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: INTERNET_AUTH_NOTIFY_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - FreeUrlCacheSpace
 - FreeUrlCacheSpaceA
 - FreeUrlCacheSpaceW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FreeUrlCacheSpaceA function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Clears the space in the specified URL cache.


## -parameters




### -param lpszCachePath

Path to the cache.


### -param dwSize

The size of the space to clear.


### -param dwFilter [in]

Filters to be used. 


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.



