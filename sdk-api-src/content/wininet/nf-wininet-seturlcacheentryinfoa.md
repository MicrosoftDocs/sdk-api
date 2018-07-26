---
UID: NF:wininet.SetUrlCacheEntryInfoA
title: SetUrlCacheEntryInfoA function
author: windows-sdk-content
description: Sets the specified members of the INTERNET_CACHE_ENTRY_INFO structure.
old-location: wininet\seturlcacheentryinfo.htm
old-project: wininet
ms.assetid: 71f6e1a3-09ce-4576-9480-1270f343db39
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: SetUrlCacheEntryInfo, SetUrlCacheEntryInfo function [WinINet], SetUrlCacheEntryInfoA, SetUrlCacheEntryInfoW, _inet_seturlcacheentryinfo_function, wininet.seturlcacheentryinfo, wininet/SetUrlCacheEntryInfo, wininet/SetUrlCacheEntryInfoA, wininet/SetUrlCacheEntryInfoW
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
req.unicode-ansi: SetUrlCacheEntryInfoW (Unicode) and SetUrlCacheEntryInfoA (ANSI)
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
 - SetUrlCacheEntryInfo
 - SetUrlCacheEntryInfoA
 - SetUrlCacheEntryInfoW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetUrlCacheEntryInfoA function


## -description


Sets the specified members of the 
<a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure.


## -parameters




### -param lpszUrlName [in]

Pointer to a null-terminated string that specifies the name of the cache entry. The name string should not contain any escape characters.


### -param lpCacheEntryInfo [in]

Pointer to an 
<a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure containing the values to be assigned to the cache entry designated by 
<i>lpszUrlName</i>.


### -param dwFieldControl [in]

Indicates the members that are to be set. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_ACCTIME_FC</dt>
</dl>
</td>
<td width="60%">
Sets the last access time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_ATTRIBUTE_FC</dt>
</dl>
</td>
<td width="60%">
Sets the cache entry type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_EXEMPT_DELTA_FC</dt>
</dl>
</td>
<td width="60%">
Sets the exempt delta.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_EXPTIME_FC</dt>
</dl>
</td>
<td width="60%">
Sets the expire time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_HEADERINFO_FC</dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_HITRATE_FC</dt>
</dl>
</td>
<td width="60%">
Sets the hit rate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_MODTIME_FC</dt>
</dl>
</td>
<td width="60%">
Sets the last modified time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHE_ENTRY_SYNCTIME_FC</dt>
</dl>
</td>
<td width="60%">
Sets the last sync time.

</td>
</tr>
</table>
 


## -returns



Returns TRUE if successful, or FALSE otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified cache entry is not found in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value(s) to be set is invalid.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

