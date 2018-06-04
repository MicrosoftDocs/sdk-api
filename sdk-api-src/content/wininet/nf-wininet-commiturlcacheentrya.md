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

# CommitUrlCacheEntryA function


## -description


Stores data in the specified file in the Internet cache and associates it with the specified URL.


## -parameters




### -param lpszUrlName [in]

Pointer to a string variable that contains the source name of the cache entry. The name string must be unique and should not contain any escape characters.


### -param lpszLocalFileName [in]

Pointer to a string variable that contains the name of the local file that is being cached. This should be the same name as that returned by 
<b>CreateUrlCacheEntryA</b>.


### -param ExpireTime [in]


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the expire date and time (in Greenwich mean time) of the file that is being cached. If the expire date and time is unknown, set this parameter to zero.


### -param LastModifiedTime [in]


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the last modified date and time (in Greenwich mean time) of the URL that is being cached. If the last modified date and time is unknown, set this parameter to zero.


### -param CacheEntryType [in]

A bitmask indicating the type of cache entry and its properties. The cache entry types include: history entries (URLHISTORY_CACHE_ENTRY),  cookie entries  (COOKIE_CACHE_ENTRY), and normal cached content (NORMAL_CACHE_ENTRY).

This parameter can be zero or more of the following property flags, and  cache type flags listed below.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>COOKIE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Cookie cache entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>EDITED_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Cache entry file that has been edited externally. This cache entry type is exempt from scavenging.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>NORMAL_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Normal cache entry; can be deleted to recover space for new entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SPARSE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Partial response cache entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>STICKY_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Sticky cache entry; exempt from scavenging.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>TRACK_OFFLINE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>TRACK_ONLINE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>URLHISTORY_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Visited link cache entry.

</td>
</tr>
</table>
 


### -param lpHeaderInfo [in]

Pointer to the buffer that contains the header information. If this parameter is not <b>NULL</b>, the header information is treated as extended attributes of the URL that are returned in the <b>lpHeaderInfo</b> 
member of the <a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure.


### -param cchHeaderInfo [in]

Size of the header information, in <b>TCHARs</b>. If 
<i>lpHeaderInfo</i> is not <b>NULL</b>, this value is assumed to indicate the size of the buffer that  stores the header information. An application can maintain headers as part of the data and provide 
<i>cchHeaderInfo</i> together with a <b>NULL</b> value for 
<i>lpHeaderInfo</i>.


### -param lpszFileExtension [in]

This parameter is reserved and must be <b>NULL</b>.


### -param lpszOriginalUrl [in]

Pointer to a string  that contains the original URL, if redirection has occurred.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DISK_FULL</b></dt>
</dl>
</td>
<td width="60%">
The cache storage is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified local file is not found.

</td>
</tr>
</table>
 




## -remarks



The STICKY_CACHE_ENTRY type is used to make cache entries exempt from scavenging. The default exempt time for entries set using 
<b>CommitUrlCacheEntryA</b> is ten minutes. The exempt time can be changed by setting the expires time parameter in the <a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure in the call to the 
<a href="https://msdn.microsoft.com/71f6e1a3-09ce-4576-9480-1270f343db39">SetUrlCacheEntryInfo</a> function.

If the cache storage is full, 
<b>CommitUrlCacheEntryA</b> invokes cache cleanup to make space for this new file. If the cache entry already exists, the function overwrites the entry if it is not in use. An entry is in use when it has been retrieved with either 
<a href="https://msdn.microsoft.com/0414efb0-d91b-46f0-9fee-0b69ef823029">RetrieveUrlCacheEntryStream</a> or 
<a href="https://msdn.microsoft.com/eb311b8d-560d-4742-af4c-b5afe660c8e5">RetrieveUrlCacheEntryFile</a>.

Clients that add entries to the cache should set the headers to at least "HTTP/1.0 200 OK\r\n\r\n"; otherwise, Microsoft Internet Explorer and other client applications should disregard the entry.

See <a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a> for example code calling <b>CreateUrlCacheEntryA</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

