---
UID: NS:wincrypt._CRYPTNET_URL_CACHE_PRE_FETCH_INFO
title: CRYPTNET_URL_CACHE_PRE_FETCH_INFO (wincrypt.h)
description: Contains update information used by the Cryptnet URL Cache (CUC) service to maintain a URL cache entry.
helpviewer_keywords: ["*PCRYPTNET_URL_CACHE_PRE_FETCH_INFO","CRYPTNET_URL_CACHE_PRE_FETCH_AUTOROOT_CAB","CRYPTNET_URL_CACHE_PRE_FETCH_BLOB","CRYPTNET_URL_CACHE_PRE_FETCH_CRL","CRYPTNET_URL_CACHE_PRE_FETCH_INFO","CRYPTNET_URL_CACHE_PRE_FETCH_INFO structure [Security]","CRYPTNET_URL_CACHE_PRE_FETCH_NONE","CRYPTNET_URL_CACHE_PRE_FETCH_OCSP","ERROR_FILE_OFFLINE","ERROR_INVALID_DATA","ERROR_MEDIA_OFFLINE","Other values","PCRYPTNET_URL_CACHE_PRE_FETCH_INFO","PCRYPTNET_URL_CACHE_PRE_FETCH_INFO structure pointer [Security]","S_OK","security.cryptnet_url_cache_pre_fetch_info","szOID_CRL_NEXT_PUBLISH","wincrypt/CRYPTNET_URL_CACHE_PRE_FETCH_INFO","wincrypt/PCRYPTNET_URL_CACHE_PRE_FETCH_INFO"]
old-location: security\cryptnet_url_cache_pre_fetch_info.htm
tech.root: security
ms.assetid: 4c3e3248-83d2-45f4-84a5-a73f0434b804
ms.date: 12/05/2018
ms.keywords: '*PCRYPTNET_URL_CACHE_PRE_FETCH_INFO, CRYPTNET_URL_CACHE_PRE_FETCH_AUTOROOT_CAB, CRYPTNET_URL_CACHE_PRE_FETCH_BLOB, CRYPTNET_URL_CACHE_PRE_FETCH_CRL, CRYPTNET_URL_CACHE_PRE_FETCH_INFO, CRYPTNET_URL_CACHE_PRE_FETCH_INFO structure [Security], CRYPTNET_URL_CACHE_PRE_FETCH_NONE, CRYPTNET_URL_CACHE_PRE_FETCH_OCSP, ERROR_FILE_OFFLINE, ERROR_INVALID_DATA, ERROR_MEDIA_OFFLINE, Other values, PCRYPTNET_URL_CACHE_PRE_FETCH_INFO, PCRYPTNET_URL_CACHE_PRE_FETCH_INFO structure pointer [Security], S_OK, security.cryptnet_url_cache_pre_fetch_info, szOID_CRL_NEXT_PUBLISH, wincrypt/CRYPTNET_URL_CACHE_PRE_FETCH_INFO, wincrypt/PCRYPTNET_URL_CACHE_PRE_FETCH_INFO'
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
req.typenames: CRYPTNET_URL_CACHE_PRE_FETCH_INFO, *PCRYPTNET_URL_CACHE_PRE_FETCH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTNET_URL_CACHE_PRE_FETCH_INFO
 - wincrypt/_CRYPTNET_URL_CACHE_PRE_FETCH_INFO
 - PCRYPTNET_URL_CACHE_PRE_FETCH_INFO
 - wincrypt/PCRYPTNET_URL_CACHE_PRE_FETCH_INFO
 - CRYPTNET_URL_CACHE_PRE_FETCH_INFO
 - wincrypt/CRYPTNET_URL_CACHE_PRE_FETCH_INFO
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
 - CRYPTNET_URL_CACHE_PRE_FETCH_INFO
---

# CRYPTNET_URL_CACHE_PRE_FETCH_INFO structure


## -description

The <b>CRYPTNET_URL_CACHE_PRE_FETCH_INFO</b> structure contains update information used by the Cryptnet URL Cache (CUC) service to maintain a URL cache entry. This structure composes the <b>pPreFetchInfo</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_retrieve_aux_info">CRYPT_RETRIEVE_AUX_INFO</a> structure that is passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> function as the <i>pAuxInfo</i> parameter.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwObjectType

A value that specifies the type of object represented by the URL.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_PRE_FETCH_NONE"></a><a id="cryptnet_url_cache_pre_fetch_none"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_PRE_FETCH_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Prefetch information does not yet exist.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_PRE_FETCH_BLOB"></a><a id="cryptnet_url_cache_pre_fetch_blob"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_PRE_FETCH_BLOB</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The object is a memory <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_PRE_FETCH_CRL"></a><a id="cryptnet_url_cache_pre_fetch_crl"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_PRE_FETCH_CRL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The object is a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_PRE_FETCH_OCSP"></a><a id="cryptnet_url_cache_pre_fetch_ocsp"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_PRE_FETCH_OCSP</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The object is an <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) response.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTNET_URL_CACHE_PRE_FETCH_AUTOROOT_CAB"></a><a id="cryptnet_url_cache_pre_fetch_autoroot_cab"></a><dl>
<dt><b>CRYPTNET_URL_CACHE_PRE_FETCH_AUTOROOT_CAB</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The object is a CAB file.

</td>
</tr>
</table>

### -field dwError

A value that specifies the status of a prefetch attempt.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The prefetch is pending.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_MEDIA_OFFLINE"></a><a id="error_media_offline"></a><dl>
<dt><b>ERROR_MEDIA_OFFLINE</b></dt>
<dt>4304L</dt>
</dl>
</td>
<td width="60%">
The CRL prefetch is disabled because the OCSP service is offline or unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_FILE_OFFLINE"></a><a id="error_file_offline"></a><dl>
<dt><b>ERROR_FILE_OFFLINE</b></dt>
<dt>4350L</dt>
</dl>
</td>
<td width="60%">
The prefetch content is unchanged.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_INVALID_DATA"></a><a id="error_invalid_data"></a><dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
<dt>13L</dt>
</dl>
</td>
<td width="60%">
The prefetch content is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="Other_values"></a><a id="other_values"></a><a id="OTHER_VALUES"></a><dl>
<dt><b>Other values</b></dt>
</dl>
</td>
<td width="60%">
The service is unable to retrieve prefetch content.

</td>
</tr>
</table>

### -field dwReserved

This parameter is not used. It must be zero.

### -field ThisUpdateTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains a date and time whose meaning depends on <b>dwObjectType</b>. For a CRL, this indicates when the CRL was published. For an OCSP response, this indicates when the indicated status is known to be correct.

### -field NextUpdateTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains a date and time whose meaning depends on <b>dwObjectType</b>. For a CRL, this indicates the next scheduled update for the CRL. For an OCSP response, this indicates when newer information will be available for the certificate status.

This is effectively an expiry date for the object. A value of zero indicates that the information has no expiration date.

### -field PublishTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the time interval before expiry that a new CRL will be published. This value can be zero.

This value is based on a nonstandard CRL extension with the following <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_CRL_NEXT_PUBLISH"></a><a id="szoid_crl_next_publish"></a><a id="SZOID_CRL_NEXT_PUBLISH"></a><dl>
<dt><b>szOID_CRL_NEXT_PUBLISH</b></dt>
<dt>1.3.6.1.4.1.311.21.4</dt>
</dl>
</td>
<td width="60%">
NextPublishTime

</td>
</tr>
</table>