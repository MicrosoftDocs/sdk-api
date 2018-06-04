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

# _CRYPTNET_URL_CACHE_FLUSH_INFO structure


## -description


The <b>CRYPTNET_URL_CACHE_FLUSH_INFO</b> structure contains expiry information used by the Cryptnet URL Cache (CUC) service to maintain a URL cache entry. This structure composes the <b>pFlushInfo</b> member of the <a href="https://msdn.microsoft.com/33ea51e7-c3e3-4cf8-ade0-099cb8b2e651">CRYPT_RETRIEVE_AUX_INFO</a> structure that is passed to the <a href="https://msdn.microsoft.com/2e205f97-be9b-4358-ba22-d475b6a250b7">CryptRetrieveObjectByUrl</a> method as the <i>pAuxInfo</i> parameter.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field dwExemptSeconds

A value that specifies how long to extend the <b>ExpireTime</b> member. If prefetch is enabled, the CUC service ignores this value.


The following values have special meaning.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_DEFAULT_FLUSH"></a><a id="cryptnet_url_cache_default_flush"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_DEFAULT_FLUSH</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Use the default flush exempt seconds for a retrieved URL. The following <b>REG_DWORD</b> constants define the default value of dwExemptSeconds for a computer.

<dl>
<dt>CRYPTNET_URL_CACHE_DEFAULT_FLUSH_EXEMPT_SECONDS_VALUE_NAME L"CryptnetDefaultFlushExemptSeconds"</dt>
<dt>CRYPTNET_URL_CACHE_DEFAULT_FLUSH_EXEMPT_SECONDS_DEFAULT (28 * 24 * 60 * 60)</dt>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_DISABLE_FLUSH"></a><a id="cryptnet_url_cache_disable_flush"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_DISABLE_FLUSH</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
Disable cache flushing for a retrieved URL.

</td>
</tr>
</table>
 


### -field ExpireTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time the object expires.


## -remarks



The <b>dwExemptSeconds</b> member is added to the <b>ExpireTime</b> member to determine the flush time. If the <b>pLastSyncTime</b> member of the <a href="https://msdn.microsoft.com/33ea51e7-c3e3-4cf8-ade0-099cb8b2e651">CRYPT_RETRIEVE_AUX_INFO</a> structure  is after the <b>ExpireTime</b> member, the <b>pLastSyncTime</b> member  determines the flush time.



