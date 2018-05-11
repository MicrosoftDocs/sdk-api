---
UID: NS:wininet._INTERNET_CACHE_ENTRY_INFOW
title: "_INTERNET_CACHE_ENTRY_INFOW"
author: windows-driver-content
description: Contains information about an entry in the Internet cache.
old-location: wininet\internet_cache_entry_info.htm
old-project: WinInet
ms.assetid: 7bda08e0-5df0-4087-a5cd-3a25c6ae5ade
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "*LPINTERNET_CACHE_ENTRY_INFOW, COOKIE_CACHE_ENTRY, EDITED_CACHE_ENTRY, INTERNET_CACHE_ENTRY_INFO, INTERNET_CACHE_ENTRY_INFO structure [WinINet], INTERNET_CACHE_ENTRY_INFOA, INTERNET_CACHE_ENTRY_INFOW, LPINTERNET_CACHE_ENTRY_INFO, LPINTERNET_CACHE_ENTRY_INFO structure pointer [WinINet], NORMAL_CACHE_ENTRY, SPARSE_CACHE_ENTRY, STICKY_CACHE_ENTRY, TRACK_OFFLINE_CACHE_ENTRY, TRACK_ONLINE_CACHE_ENTRY, URLHISTORY_CACHE_ENTRY, _INTERNET_CACHE_ENTRY_INFOW, _inet_internet_cache_entry_info_structure, wininet.internet_cache_entry_info, wininet/INTERNET_CACHE_ENTRY_INFO, wininet/INTERNET_CACHE_ENTRY_INFOA, wininet/INTERNET_CACHE_ENTRY_INFOW, wininet/LPINTERNET_CACHE_ENTRY_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INTERNET_CACHE_ENTRY_INFOW (Unicode) and INTERNET_CACHE_ENTRY_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: INTERNET_CACHE_ENTRY_INFOW, *LPINTERNET_CACHE_ENTRY_INFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wininet.h
api_name:
-	INTERNET_CACHE_ENTRY_INFO
-	INTERNET_CACHE_ENTRY_INFOA
-	INTERNET_CACHE_ENTRY_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _INTERNET_CACHE_ENTRY_INFOW structure


## -description


Contains information about an entry in the Internet cache.


## -struct-fields




### -field dwStructSize

Size of this structure, in bytes. This value can be used to help determine the version of the cache system. 


### -field lpszSourceUrlName

Pointer to a null-terminated string that contains the URL name. The string occupies the memory area at the end of this structure. 


### -field lpszLocalFileName

Pointer to a null-terminated string that contains the local file name. The string occupies the memory area at the end of this structure. 


### -field CacheEntryType

A bitmask indicating the type of cache entry and its properties. The cache entry types include: history entries (URLHISTORY_CACHE_ENTRY),  cookie entries  (COOKIE_CACHE_ENTRY), and normal cached content (NORMAL_CACHE_ENTRY).


This member can be zero or more of the following property flags, and  cache type flags listed below.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EDITED_CACHE_ENTRY"></a><a id="edited_cache_entry"></a><dl>
<dt><b>EDITED_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Cache entry file that has been edited externally. This cache entry type is exempt from scavenging.

</td>
</tr>
<tr>
<td width="40%"><a id="SPARSE_CACHE_ENTRY"></a><a id="sparse_cache_entry"></a><dl>
<dt><b>SPARSE_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Partial response cache entry.

</td>
</tr>
<tr>
<td width="40%"><a id="STICKY_CACHE_ENTRY"></a><a id="sticky_cache_entry"></a><dl>
<dt><b>STICKY_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Sticky cache entry that is exempt from scavenging for the amount of time specified by 
<b>dwExemptDelta</b>. The default value set by 
<a href="https://msdn.microsoft.com/4bd21b30-cac5-482b-9826-b5a4ffeeebe9">CommitUrlCacheEntryA</a> and <a href="https://msdn.microsoft.com/0124e664-85a3-4637-9d91-7ec23025a87b">CommitUrlCacheEntryW</a> is one day. 

</td>
</tr>
<tr>
<td width="40%"><a id="TRACK_OFFLINE_CACHE_ENTRY"></a><a id="track_offline_cache_entry"></a><dl>
<dt><b>TRACK_OFFLINE_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACK_ONLINE_CACHE_ENTRY"></a><a id="track_online_cache_entry"></a><dl>
<dt><b>TRACK_ONLINE_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
</table>
 


The following list contains the cache type flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COOKIE_CACHE_ENTRY"></a><a id="cookie_cache_entry"></a><dl>
<dt><b>COOKIE_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Cookie cache entry.

</td>
</tr>
<tr>
<td width="40%"><a id="NORMAL_CACHE_ENTRY"></a><a id="normal_cache_entry"></a><dl>
<dt><b>NORMAL_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Normal cache entry; can be deleted to recover space for new entries.

</td>
</tr>
<tr>
<td width="40%"><a id="URLHISTORY_CACHE_ENTRY"></a><a id="urlhistory_cache_entry"></a><dl>
<dt><b>URLHISTORY_CACHE_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Visited link cache entry.

</td>
</tr>
</table>
 


### -field dwUseCount

Current number of WinINEet callers using the cache entry. 


### -field dwHitRate

Number of times the cache entry was retrieved. 


### -field dwSizeLow

Low-order portion of the file size, in <b>bytes</b>. 


### -field dwSizeHigh

High-order portion of the file size, in <b>bytes</b>. 


### -field LastModifiedTime


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the last modified time of this URL, in Greenwich mean time format. 


### -field ExpireTime


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the expiration time of this file, in Greenwich mean time format. 


### -field LastAccessTime


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the last accessed time, in Greenwich mean time format. 


### -field LastSyncTime


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the last time the cache was synchronized. 


### -field lpHeaderInfo

Pointer to a buffer that contains the header information. The buffer occupies the memory at the end of this structure. 


### -field dwHeaderInfoSize

Size of the 
<b>lpHeaderInfo</b> buffer, in <b>TCHARs</b>. 


### -field lpszFileExtension

Pointer to a string that contains the file name extension used to retrieve the data as a file. The string occupies the memory area at the end of this structure. 


### -field dwReserved


### -field dwExemptDelta

Exemption time from the last accessed time, in seconds. 


## -remarks



There is no cache entry size limit, so applications that need to enumerate the cache must be prepared to allocate variable-sized buffers. For more information, see 
<a href="https://msdn.microsoft.com/ae7f84ba-15d4-483b-bdda-0042854f9e1b">Using Buffers</a>.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e8407284-846b-4080-b75b-4805330e0f95">FindFirstUrlCacheEntry</a>



<a href="https://msdn.microsoft.com/af17c809-2a9e-443a-b64a-93c028e3b71b">FindFirstUrlCacheEntryEx</a>



<a href="https://msdn.microsoft.com/776bf73e-00f3-46a1-a8c7-5eb365e9a518">FindNextUrlCacheEntry</a>



<a href="https://msdn.microsoft.com/39484e35-cd25-4e48-ace0-16033d3e6954">FindNextUrlCacheEntryEx</a>



<a href="https://msdn.microsoft.com/0f70bcef-2d56-4765-a44e-4549b4ae2ced">GetUrlCacheEntryInfo</a>



<a href="https://msdn.microsoft.com/3842dae9-9474-492a-83fa-29d7927dc92d">GetUrlCacheEntryInfoEx</a>



<a href="https://msdn.microsoft.com/71f6e1a3-09ce-4576-9480-1270f343db39">SetUrlCacheEntryInfo</a>
 

 

