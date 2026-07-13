---
UID: NF:wininet.SetUrlCacheEntryGroupW
title: SetUrlCacheEntryGroupW function (wininet.h)
description: The SetUrlCacheEntryGroupW (Unicode) function (wininet.h) adds entries to or removes entries from a cache group.
helpviewer_keywords: ["SetUrlCacheEntryGroup", "SetUrlCacheEntryGroup function [WinINet]", "SetUrlCacheEntryGroupW", "_inet_seturlcacheentrygroup_function", "wininet.seturlcacheentrygroup", "wininet/SetUrlCacheEntryGroup", "wininet/SetUrlCacheEntryGroupW"]
old-location: wininet\seturlcacheentrygroup.htm
tech.root: wininet
ms.assetid: b39a96ac-c5b5-4b02-88e2-298a037be25f
ms.date: 08/10/2022
ms.keywords: SetUrlCacheEntryGroup, SetUrlCacheEntryGroup function [WinINet], SetUrlCacheEntryGroupA, SetUrlCacheEntryGroupW, _inet_seturlcacheentrygroup_function, wininet.seturlcacheentrygroup, wininet/SetUrlCacheEntryGroup, wininet/SetUrlCacheEntryGroupA, wininet/SetUrlCacheEntryGroupW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetUrlCacheEntryGroupW (Unicode) and SetUrlCacheEntryGroupA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetUrlCacheEntryGroupW
 - wininet/SetUrlCacheEntryGroupW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - SetUrlCacheEntryGroup
 - SetUrlCacheEntryGroupA
 - SetUrlCacheEntryGroupW
---

# SetUrlCacheEntryGroupW function


## -description

Adds entries to or removes entries from a cache group.

## -parameters

### -param lpszUrlName [in]

Pointer to a <b>null</b>-terminated string value that specifies the URL of the cached resource.

### -param dwFlags [in]

Determines whether the entry is added to or removed from a cache group. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_CACHE_GROUP_ADD</dt>
</dl>
</td>
<td width="60%">
Adds the cache entry to the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_CACHE_GROUP_REMOVE</dt>
</dl>
</td>
<td width="60%">
Removes the entry from the cache group.

</td>
</tr>
</table>

### -param GroupId [in]

Identifier of the cache group that the entry will be added to or removed from.

### -param pbGroupAttributes [in]

This parameter is reserved and must be <b>NULL</b>.

### -param cbGroupAttributes [in]

This parameter is reserved and must be 0.

### -param lpReserved [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

A cache entry can belong to more than one cache group.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines SetUrlCacheEntryGroup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
