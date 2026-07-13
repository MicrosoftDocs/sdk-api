---
UID: NF:winineti.GetUrlCacheConfigInfoW
title: GetUrlCacheConfigInfoW function (winineti.h)
description: Retrieves information about cache configuration. (Unicode)
helpviewer_keywords: ["CACHE_CONFIG_CONTENT_PATHS_FC", "CACHE_CONFIG_CONTENT_USAGE_FC", "CACHE_CONFIG_COOKIES_PATHS_FC", "CACHE_CONFIG_DISK_CACHE_PATHS_FC", "CACHE_CONFIG_FORCE_CLEANUP_FC", "CACHE_CONFIG_HISTORY_PATHS_FC", "CACHE_CONFIG_QUOTA_FC", "CACHE_CONFIG_STICKY_CONTENT_USAGE_FC", "CACHE_CONFIG_SYNC_MODE_FC", "CACHE_CONFIG_USER_MODE_FC", "GetUrlCacheConfigInfo", "GetUrlCacheConfigInfo function [WinINet]", "GetUrlCacheConfigInfoW", "wininet.geturlcacheconfiginfo", "winineti/GetUrlCacheConfigInfo", "winineti/GetUrlCacheConfigInfoW"]
old-location: wininet\geturlcacheconfiginfo.htm
tech.root: wininet
ms.assetid: 93a29a4f-57bf-497c-a7b1-3960935590f9
ms.date: 12/05/2018
ms.keywords: CACHE_CONFIG_CONTENT_PATHS_FC, CACHE_CONFIG_CONTENT_USAGE_FC, CACHE_CONFIG_COOKIES_PATHS_FC, CACHE_CONFIG_DISK_CACHE_PATHS_FC, CACHE_CONFIG_FORCE_CLEANUP_FC, CACHE_CONFIG_HISTORY_PATHS_FC, CACHE_CONFIG_QUOTA_FC, CACHE_CONFIG_STICKY_CONTENT_USAGE_FC, CACHE_CONFIG_SYNC_MODE_FC, CACHE_CONFIG_USER_MODE_FC, GetUrlCacheConfigInfo, GetUrlCacheConfigInfo function [WinINet], GetUrlCacheConfigInfoA, GetUrlCacheConfigInfoW, wininet.geturlcacheconfiginfo, winineti/GetUrlCacheConfigInfo, winineti/GetUrlCacheConfigInfoA, winineti/GetUrlCacheConfigInfoW
req.header: winineti.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP4 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP4 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUrlCacheConfigInfoW (Unicode) and GetUrlCacheConfigInfoA (ANSI)
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
 - GetUrlCacheConfigInfoW
 - winineti/GetUrlCacheConfigInfoW
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
 - GetUrlCacheConfigInfo
 - GetUrlCacheConfigInfoA
 - GetUrlCacheConfigInfoW
---

# GetUrlCacheConfigInfoW function


## -description

Retrieves information about cache configuration.

## -parameters

### -param lpCacheConfigInfo [in, out]

A pointer to an 
       <a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a> structure 
       that receives information about the cache configuration. The <b>dwStructSize</b> field of 
       the structure should be initialized to the size of 
       <b>INTERNET_CACHE_CONFIG_INFO</b>.

### -param lpcbCacheConfigInfo

This parameter is reserved and must be <b>NULL</b>.

### -param dwFieldControl [in]

Determines the behavior of the function, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_FORCE_CLEANUP_FC"></a><a id="cache_config_force_cleanup_fc"></a><dl>
<dt><b>CACHE_CONFIG_FORCE_CLEANUP_FC</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_DISK_CACHE_PATHS_FC"></a><a id="cache_config_disk_cache_paths_fc"></a><dl>
<dt><b>CACHE_CONFIG_DISK_CACHE_PATHS_FC</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_SYNC_MODE_FC"></a><a id="cache_config_sync_mode_fc"></a><dl>
<dt><b>CACHE_CONFIG_SYNC_MODE_FC</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_CONTENT_PATHS_FC"></a><a id="cache_config_content_paths_fc"></a><dl>
<dt><b>CACHE_CONFIG_CONTENT_PATHS_FC</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The <b>CachePath</b> field of the 
         <a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a> structure 
         specified in the <i>lpCachedConfigInfo</i> parameter is filled with a pointer to a string 
         identifying the content path. This cannot be used at the same time as 
         <b>CACHE_CONFIG_HISTORY_PATHS_FC</b> or 
         <b>CACHE_CONFIG_COOKIES_PATHS_FC</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_HISTORY_PATHS_FC"></a><a id="cache_config_history_paths_fc"></a><dl>
<dt><b>CACHE_CONFIG_HISTORY_PATHS_FC</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The <b>CachePath</b> field of the 
         <a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a> structure 
         specified in the <i>lpCachedConfigInfo</i> parameter is filled with a pointer to a string 
         identifying the history path. This cannot be used at the same time as 
         <b>CACHE_CONFIG_CONTENT_PATHS_FC</b> or 
         <b>CACHE_CONFIG_COOKIES_PATHS_FC</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_COOKIES_PATHS_FC"></a><a id="cache_config_cookies_paths_fc"></a><dl>
<dt><b>CACHE_CONFIG_COOKIES_PATHS_FC</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The <b>CachePath</b> field of the 
         <a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a> structure 
         specified in the <i>lpCachedConfigInfo</i> parameter is filled with a pointer to a string 
         identifying the cookie path. This cannot be used at the same time as 
         <b>CACHE_CONFIG_CONTENT_PATHS_FC</b> or 
         <b>CACHE_CONFIG_HISTORY_PATHS_FC</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_QUOTA_FC"></a><a id="cache_config_quota_fc"></a><dl>
<dt><b>CACHE_CONFIG_QUOTA_FC</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The <b>dwQuota</b> field of the 
         <a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a> structure 
         specified in the <i>lpCachedConfigInfo</i> is set to the cache limit for the container 
         specified in the <b>dwContainer</b> field.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_USER_MODE_FC"></a><a id="cache_config_user_mode_fc"></a><dl>
<dt><b>CACHE_CONFIG_USER_MODE_FC</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_CONTENT_USAGE_FC"></a><a id="cache_config_content_usage_fc"></a><dl>
<dt><b>CACHE_CONFIG_CONTENT_USAGE_FC</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The <b>dwNormalUsage</b> field of the 
         <a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a> structure 
         specified in the <i>lpCachedConfigInfo</i> is set to the cache size for the container 
         specified in the <b>dwContainer</b> field.

</td>
</tr>
<tr>
<td width="40%"><a id="CACHE_CONFIG_STICKY_CONTENT_USAGE_FC"></a><a id="cache_config_sticky_content_usage_fc"></a><dl>
<dt><b>CACHE_CONFIG_STICKY_CONTENT_USAGE_FC</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
The <b>dwExemptUsage</b> field of the 
         <a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a> structure 
         specified in the <i>lpCachedConfigInfo</i> is set to the exempt usage, the amount of bytes 
         exempt from scavenging, for the container specified in the <b>dwContainer</b> field. (This 
         field must be the content container.)

</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get 
       extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The winineti.h header defines GetUrlCacheConfigInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winineti/ns-winineti-internet_cache_config_infoa">INTERNET_CACHE_CONFIG_INFO</a>
