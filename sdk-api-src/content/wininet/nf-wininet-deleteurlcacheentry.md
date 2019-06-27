---
UID: NF:wininet.DeleteUrlCacheEntry
title: DeleteUrlCacheEntry function (wininet.h)
author: windows-sdk-content
description: Removes the file associated with the source name from the cache, if the file exists.
old-location: wininet\deleteurlcacheentry.htm
tech.root: wininet
ms.assetid: bb765cba-6662-4dca-8f9f-3f35e37da28a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteUrlCacheEntry, DeleteUrlCacheEntry function [WinINet], DeleteUrlCacheEntryA, DeleteUrlCacheEntryW, _inet_deleteurlcacheentry_function, wininet.deleteurlcacheentry, wininet/DeleteUrlCacheEntry, wininet/DeleteUrlCacheEntryA, wininet/DeleteUrlCacheEntryW
ms.topic: function
f1_keywords: 
 - "wininet/DeleteUrlCacheEntry"
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteUrlCacheEntryW (Unicode) and DeleteUrlCacheEntryA (ANSI)
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
 - DeleteUrlCacheEntry
 - DeleteUrlCacheEntryA
 - DeleteUrlCacheEntryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteUrlCacheEntry function


## -description


Removes the file associated with the source name from the cache, if the file exists.


## -parameters




### -param lpszUrlName [in]

Pointer to a string that contains the name of the source that corresponds to the cache entry.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The file is locked or in use. The entry is marked and  deleted when the file is unlocked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file is not in the cache.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/caching">Caching</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

