---
UID: NS:wincrypt._CRYPTNET_URL_CACHE_RESPONSE_INFO
title: CRYPTNET_URL_CACHE_RESPONSE_INFO (wincrypt.h)
description: Contains response information used by the Cryptnet URL Cache (CUC) service to maintain a URL cache entry.
helpviewer_keywords: ["*PCRYPTNET_URL_CACHE_RESPONSE_INFO","CRYPTNET_URL_CACHE_RESPONSE_HTTP","CRYPTNET_URL_CACHE_RESPONSE_INFO","CRYPTNET_URL_CACHE_RESPONSE_INFO structure [Security]","CRYPTNET_URL_CACHE_RESPONSE_NONE","PCRYPTNET_URL_CACHE_RESPONSE_INFO","PCRYPTNET_URL_CACHE_RESPONSE_INFO structure pointer [Security]","security.cryptnet_url_cache_response_info","wincrypt/CRYPTNET_URL_CACHE_RESPONSE_INFO","wincrypt/PCRYPTNET_URL_CACHE_RESPONSE_INFO"]
old-location: security\cryptnet_url_cache_response_info.htm
tech.root: security
ms.assetid: 26cd6065-8be9-4b3b-8207-5ad620e9b537
ms.date: 12/05/2018
ms.keywords: '*PCRYPTNET_URL_CACHE_RESPONSE_INFO, CRYPTNET_URL_CACHE_RESPONSE_HTTP, CRYPTNET_URL_CACHE_RESPONSE_INFO, CRYPTNET_URL_CACHE_RESPONSE_INFO structure [Security], CRYPTNET_URL_CACHE_RESPONSE_NONE, PCRYPTNET_URL_CACHE_RESPONSE_INFO, PCRYPTNET_URL_CACHE_RESPONSE_INFO structure pointer [Security], security.cryptnet_url_cache_response_info, wincrypt/CRYPTNET_URL_CACHE_RESPONSE_INFO, wincrypt/PCRYPTNET_URL_CACHE_RESPONSE_INFO'
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
req.typenames: CRYPTNET_URL_CACHE_RESPONSE_INFO, *PCRYPTNET_URL_CACHE_RESPONSE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTNET_URL_CACHE_RESPONSE_INFO
 - wincrypt/_CRYPTNET_URL_CACHE_RESPONSE_INFO
 - PCRYPTNET_URL_CACHE_RESPONSE_INFO
 - wincrypt/PCRYPTNET_URL_CACHE_RESPONSE_INFO
 - CRYPTNET_URL_CACHE_RESPONSE_INFO
 - wincrypt/CRYPTNET_URL_CACHE_RESPONSE_INFO
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
 - CRYPTNET_URL_CACHE_RESPONSE_INFO
---

# CRYPTNET_URL_CACHE_RESPONSE_INFO structure


## -description

The <b>CRYPTNET_URL_CACHE_RESPONSE_INFO</b> structure contains response information used by the Cryptnet URL Cache (CUC) service to maintain a URL cache entry. This structure composes the <b>pResponseInfo</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_retrieve_aux_info">CRYPT_RETRIEVE_AUX_INFO</a> structure, which is passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> as the <i>pAuxInfo</i> parameter.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field wResponseType

A value that indicates whether the cache entry contains HTTP response information.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_RESPONSE_NONE"></a><a id="cryptnet_url_cache_response_none"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_RESPONSE_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The cache entry contains no response information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_RESPONSE_HTTP"></a><a id="cryptnet_url_cache_response_http"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_RESPONSE_HTTP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The cache entry contains response information derived from HTTP response headers.

</td>
</tr>
</table>

### -field wResponseFlags

A value that specifies a collection of flags that control server-based certificate validation response options.

### -field LastModifiedTime

A <b>FILETIME</b> structure that specifies the <b>Last-Modified</b> entity-header field value  of the cached HTTP response for the URL.

### -field dwMaxAge

A value that specifies the number of seconds in the <b>max-age</b> directive  of the <b>Cache-Control</b> header of the cached HTTP response for the URL.

### -field pwszETag

A pointer to a string that contains the <b>ETag</b> response-header field value of the cached HTTP response for the URL.

### -field dwProxyId

A value that contains the MD5 hash of the HTTP response header values <b>Via</b>, <b>ETag</b>, and <b>Last-Modified</b>, if they exist.

## -remarks

If not specified in the HTTP response headers, the cache service sets the values of the <b>LastModifiedTime</b>, <b>dwMaxAge</b>, <b>pwszETag</b>, and <b>dwProxyId</b> members to zero.

The cache service only allows a strong <b>ETag</b> in the <b>pwszETag</b> member.

To determine whether a response is valid, the cache service performs a bitwise <b>AND</b> of the <b>wResponseFlags</b> member with the following constant defined in Wincrypt.h. If the result is <b>TRUE</b>, the response is valid.

<table>
<tr>
<th>Name</th>
<th>Value</th>
</tr>
<tr>
<td>CRYPTNET_URL_CACHE_RESPONSE_VALIDATED</td>
<td>0x8000</td>
</tr>
</table>