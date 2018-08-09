---
UID: NF:wininet.UnlockUrlCacheEntryStream
title: UnlockUrlCacheEntryStream function
author: windows-sdk-content
description: Closes the stream that has been retrieved using the RetrieveUrlCacheEntryStream function.
old-location: wininet\unlockurlcacheentrystream.htm
old-project: wininet
ms.assetid: 9fcc257e-732c-4545-a81b-7db20a98e497
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UnlockUrlCacheEntryStream, UnlockUrlCacheEntryStream function [WinINet], _inet_unlockurlcacheentrystream_function, wininet.unlockurlcacheentrystream, wininet/UnlockUrlCacheEntryStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
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
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - UnlockUrlCacheEntryStream
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# UnlockUrlCacheEntryStream function


## -description


Closes the stream that has been retrieved using the 
<a href="https://msdn.microsoft.com/0414efb0-d91b-46f0-9fee-0b69ef823029">RetrieveUrlCacheEntryStream</a> function.


## -parameters




### -param hUrlCacheStream [in]

Handle that was returned by the 
<a href="https://msdn.microsoft.com/0414efb0-d91b-46f0-9fee-0b69ef823029">RetrieveUrlCacheEntryStream</a> function.


### -param Reserved [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

