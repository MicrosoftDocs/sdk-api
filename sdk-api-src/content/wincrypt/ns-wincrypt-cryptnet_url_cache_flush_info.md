---
UID: NS:wincrypt._CRYPTNET_URL_CACHE_FLUSH_INFO
title: CRYPTNET_URL_CACHE_FLUSH_INFO (wincrypt.h)
description: Contains expiry information used by the Cryptnet URL Cache (CUC) service to maintain a URL cache entry.
helpviewer_keywords: ["*PCRYPTNET_URL_CACHE_FLUSH_INFO","CRYPTNET_URL_CACHE_DEFAULT_FLUSH","CRYPTNET_URL_CACHE_DISABLE_FLUSH","CRYPTNET_URL_CACHE_FLUSH_INFO","CRYPTNET_URL_CACHE_FLUSH_INFO structure [Security]","PCRYPTNET_URL_CACHE_FLUSH_INFO","PCRYPTNET_URL_CACHE_FLUSH_INFO structure pointer [Security]","security.cryptnet_url_cache_flush_info","wincrypt/CRYPTNET_URL_CACHE_FLUSH_INFO","wincrypt/PCRYPTNET_URL_CACHE_FLUSH_INFO"]
old-location: security\cryptnet_url_cache_flush_info.htm
tech.root: security
ms.assetid: 68b52dbe-c521-4281-9a00-d91ee14dd697
ms.date: 12/05/2018
ms.keywords: '*PCRYPTNET_URL_CACHE_FLUSH_INFO, CRYPTNET_URL_CACHE_DEFAULT_FLUSH, CRYPTNET_URL_CACHE_DISABLE_FLUSH, CRYPTNET_URL_CACHE_FLUSH_INFO, CRYPTNET_URL_CACHE_FLUSH_INFO structure [Security], PCRYPTNET_URL_CACHE_FLUSH_INFO, PCRYPTNET_URL_CACHE_FLUSH_INFO structure pointer [Security], security.cryptnet_url_cache_flush_info, wincrypt/CRYPTNET_URL_CACHE_FLUSH_INFO, wincrypt/PCRYPTNET_URL_CACHE_FLUSH_INFO'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPTNET_URL_CACHE_FLUSH_INFO, *PCRYPTNET_URL_CACHE_FLUSH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTNET_URL_CACHE_FLUSH_INFO
 - wincrypt/_CRYPTNET_URL_CACHE_FLUSH_INFO
 - PCRYPTNET_URL_CACHE_FLUSH_INFO
 - wincrypt/PCRYPTNET_URL_CACHE_FLUSH_INFO
 - CRYPTNET_URL_CACHE_FLUSH_INFO
 - wincrypt/CRYPTNET_URL_CACHE_FLUSH_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPTNET_URL_CACHE_FLUSH_INFO
---

# CRYPTNET_URL_CACHE_FLUSH_INFO structure


## -description

The <b>CRYPTNET_URL_CACHE_FLUSH_INFO</b> structure contains expiry information used by the Cryptnet URL Cache (CUC) service to maintain a URL cache entry. This structure composes the <b>pFlushInfo</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_retrieve_aux_info">CRYPT_RETRIEVE_AUX_INFO</a> structure that is passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> method as the <i>pAuxInfo</i> parameter.

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

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time the object expires.

## -remarks

The <b>dwExemptSeconds</b> member is added to the <b>ExpireTime</b> member to determine the flush time. If the <b>pLastSyncTime</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_retrieve_aux_info">CRYPT_RETRIEVE_AUX_INFO</a> structure  is after the <b>ExpireTime</b> member, the <b>pLastSyncTime</b> member  determines the flush time.