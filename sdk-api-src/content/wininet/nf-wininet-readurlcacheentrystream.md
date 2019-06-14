---
UID: NF:wininet.ReadUrlCacheEntryStream
title: ReadUrlCacheEntryStream function (wininet.h)
author: windows-sdk-content
description: Reads the cached data from a stream that has been opened using the RetrieveUrlCacheEntryStream function.
old-location: wininet\readurlcacheentrystream.htm
tech.root: wininet
ms.assetid: 8cfd0c64-25ca-4f08-b9b3-2743ded18030
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ReadUrlCacheEntryStream, ReadUrlCacheEntryStream function [WinINet], _inet_readurlcacheentrystream_function, wininet.readurlcacheentrystream, wininet/ReadUrlCacheEntryStream
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
 - ReadUrlCacheEntryStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReadUrlCacheEntryStream function


## -description


Reads the cached data from a stream that has been opened using the 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-retrieveurlcacheentrystreama">RetrieveUrlCacheEntryStream</a> function.


## -parameters




### -param hUrlCacheStream [in]

Handle that was returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-retrieveurlcacheentrystreama">RetrieveUrlCacheEntryStream</a> function.


### -param dwLocation [in]

Offset to be read from.


### -param lpBuffer [in, out]

Pointer to a buffer that receives the data.


### -param lpdwLen [in, out]

Pointer to a  variable that specifies the size of the 
<i>lpBuffer</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the required size of the buffer, in bytes.


### -param Reserved [in]

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If the buffer size is not sufficient, 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER and sets 
<i>lpdwLen</i> to the size necessary to contain all the information.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/caching">Caching</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

