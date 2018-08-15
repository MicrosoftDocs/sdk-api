---
UID: NF:wininet.DeleteUrlCacheEntryA
title: DeleteUrlCacheEntryA function
author: windows-sdk-content
description: Removes the file associated with the source name from the cache, if the file exists.
old-location: wininet\deleteurlcacheentry.htm
old-project: wininet
ms.assetid: bb765cba-6662-4dca-8f9f-3f35e37da28a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DeleteUrlCacheEntry, DeleteUrlCacheEntry function [WinINet], DeleteUrlCacheEntryA, DeleteUrlCacheEntryW, _inet_deleteurlcacheentry_function, wininet.deleteurlcacheentry, wininet/DeleteUrlCacheEntry, wininet/DeleteUrlCacheEntryA, wininet/DeleteUrlCacheEntryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.redist: 
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
 - DeleteUrlCacheEntry
 - DeleteUrlCacheEntryA
 - DeleteUrlCacheEntryW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteUrlCacheEntryA function


## -description


Removes the file associated with the source name from the cache, if the file exists.


## -parameters




### -param lpszUrlName [in]

Pointer to a string that contains the name of the source that corresponds to the cache entry.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include the following.

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



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

