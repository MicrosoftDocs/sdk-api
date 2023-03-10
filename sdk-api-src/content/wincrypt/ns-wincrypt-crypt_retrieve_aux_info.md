---
UID: NS:wincrypt._CRYPT_RETRIEVE_AUX_INFO
title: CRYPT_RETRIEVE_AUX_INFO (wincrypt.h)
description: Contains optional information to pass to the CryptRetrieveObjectByUrl function.
helpviewer_keywords: ["*PCRYPT_RETRIEVE_AUX_INFO","CRYPT_RETRIEVE_AUX_INFO","CRYPT_RETRIEVE_AUX_INFO structure [Security]","PCRYPT_RETRIEVE_AUX_INFO","PCRYPT_RETRIEVE_AUX_INFO structure pointer [Security]","_crypto2_crypt_retrieve_aux_info","security.crypt_retrieve_aux_info","wincrypt/CRYPT_RETRIEVE_AUX_INFO","wincrypt/PCRYPT_RETRIEVE_AUX_INFO"]
old-location: security\crypt_retrieve_aux_info.htm
tech.root: security
ms.assetid: 33ea51e7-c3e3-4cf8-ade0-099cb8b2e651
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_RETRIEVE_AUX_INFO, CRYPT_RETRIEVE_AUX_INFO, CRYPT_RETRIEVE_AUX_INFO structure [Security], PCRYPT_RETRIEVE_AUX_INFO, PCRYPT_RETRIEVE_AUX_INFO structure pointer [Security], _crypto2_crypt_retrieve_aux_info, security.crypt_retrieve_aux_info, wincrypt/CRYPT_RETRIEVE_AUX_INFO, wincrypt/PCRYPT_RETRIEVE_AUX_INFO'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPT_RETRIEVE_AUX_INFO, *PCRYPT_RETRIEVE_AUX_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_RETRIEVE_AUX_INFO
 - wincrypt/_CRYPT_RETRIEVE_AUX_INFO
 - PCRYPT_RETRIEVE_AUX_INFO
 - wincrypt/PCRYPT_RETRIEVE_AUX_INFO
 - CRYPT_RETRIEVE_AUX_INFO
 - wincrypt/CRYPT_RETRIEVE_AUX_INFO
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
 - CRYPT_RETRIEVE_AUX_INFO
---

# CRYPT_RETRIEVE_AUX_INFO structure


## -description

The <b>CRYPT_RETRIEVE_AUX_INFO</b> structure contains optional information to pass to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> function. All unused members of this structure must contain zero.

## -struct-fields

### -field cbSize

The size, in bytes, of the structure.

### -field pLastSyncTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time of the last synchronization of the data retrieved.

### -field dwMaxUrlRetrievalByteCount

A value that specifies a limit to the number of bytes retrieved. A value of zero or less specifies no limit.

### -field pPreFetchInfo

A pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cryptnet_url_cache_pre_fetch_info">CRYPTNET_URL_CACHE_PRE_FETCH_INFO</a> structure. To get prefetch information, set its <b>cbSize</b> upon input. For no prefetch information, except for <b>cbSize</b>, the data structure contains zero upon return.

### -field pFlushInfo

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cryptnet_url_cache_flush_info">CRYPTNET_URL_CACHE_FLUSH_INFO</a> structure. To get flush information, set its <b>cbSize</b> upon input. For no flush information, except for <b>cbSize</b>, the data structure
    contains zero upon return.

### -field ppResponseInfo

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cryptnet_url_cache_response_info">PCRYPTNET_URL_CACHE_RESPONSE_INFO</a> structure. To get response information, set the pointer to the address of a <b>CRYPTNET_URL_CACHE_RESPONSE_INFO</b> pointer updated with the allocated structure. For no response information, <b>ppResponseInfo</b> is set to <b>NULL</b>. If it is not <b>NULL</b>, it must be freed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

### -field pwszCacheFileNamePrefix

A pointer to a string that contains a prefix for a cached file name. If not <b>NULL</b>, the specified prefix string is concatenated to the front of the cached file name.

### -field pftCacheResync

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies a cache synchronization time. If not <b>NULL</b>, any information cached before this time is considered time invalid. For a <b>CRYPT_CACHE_ONLY_RETRIEVAL</b>, if there is a cached entry before this time, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> returns <b>ERROR_INVALID_TIME</b>. When used with an HTTP retrieval, this specifies the maximum age for a time-valid object.

### -field fProxyCacheRetrieval

A value that indicates whether <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> was called with <b>CRYPT_PROXY_CACHE_RETRIEVAL</b> set in <i>dwRetrievalFlags</i> and a proxy cache was not explicitly bypassed for the retrieval. This flag is not explicitly cleared and only applies to HTTP URL retrievals.

### -field dwHttpStatusCode

A value that specifies a status code from an unsuccessful HTTP response header. If <b>CRYPT_NOT_MODIFIED_RETRIEVAL</b> was set in <i>dwRetrievalFlags</i>, and the HTTP retrieval returns <b>HTTP_STATUS_NOT_MODIFIED</b>, this contains the <b>HTTP_STATUS_NOT_MODIFIED</b> status code. This value is not explicitly cleared and is only updated for HTTP or HTTPS URL retrievals.

### -field ppwszErrorResponseHeaders

### -field ppErrorContentBlob