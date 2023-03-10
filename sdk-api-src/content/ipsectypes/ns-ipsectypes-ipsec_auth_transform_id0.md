---
UID: NS:ipsectypes.IPSEC_AUTH_TRANSFORM_ID0_
title: IPSEC_AUTH_TRANSFORM_ID0 (ipsectypes.h)
description: Is used to uniquely identify the hash algorithm used in an IPsec security association (SA).
helpviewer_keywords: ["IPSEC_AUTH_CONFIG_GCM_AES_128","IPSEC_AUTH_CONFIG_GCM_AES_192","IPSEC_AUTH_CONFIG_GCM_AES_256","IPSEC_AUTH_CONFIG_HMAC_MD5_96","IPSEC_AUTH_CONFIG_HMAC_SHA_1_96","IPSEC_AUTH_CONFIG_HMAC_SHA_256_128","IPSEC_AUTH_TRANSFORM_ID0","IPSEC_AUTH_TRANSFORM_ID0 structure [Filtering]","fwp.ipsec_auth_transform_id0_struct","ipsectypes/IPSEC_AUTH_TRANSFORM_ID0"]
old-location: fwp\ipsec_auth_transform_id0_struct.htm
tech.root: fwp
ms.assetid: b8474e98-451d-4347-9369-367f16f83cf6
ms.date: 12/05/2018
ms.keywords: IPSEC_AUTH_CONFIG_GCM_AES_128, IPSEC_AUTH_CONFIG_GCM_AES_192, IPSEC_AUTH_CONFIG_GCM_AES_256, IPSEC_AUTH_CONFIG_HMAC_MD5_96, IPSEC_AUTH_CONFIG_HMAC_SHA_1_96, IPSEC_AUTH_CONFIG_HMAC_SHA_256_128, IPSEC_AUTH_TRANSFORM_ID0, IPSEC_AUTH_TRANSFORM_ID0 structure [Filtering], fwp.ipsec_auth_transform_id0_struct, ipsectypes/IPSEC_AUTH_TRANSFORM_ID0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_AUTH_TRANSFORM_ID0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_AUTH_TRANSFORM_ID0_
 - ipsectypes/IPSEC_AUTH_TRANSFORM_ID0_
 - IPSEC_AUTH_TRANSFORM_ID0
 - ipsectypes/IPSEC_AUTH_TRANSFORM_ID0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_AUTH_TRANSFORM_ID0
---

# IPSEC_AUTH_TRANSFORM_ID0 structure


## -description

The <b>IPSEC_AUTH_TRANSFORM_ID0</b> structure is used to uniquely identify the hash algorithm used in an IPsec security association (SA).

## -struct-fields

### -field authType

The type of the hash algorithm as specified by [IPSEC_AUTH_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_auth_type).

### -field authConfig

Additional configuration information for the IPsec SA hash algorithm as specified by a <b>IPSEC_AUTH_CONFIG</b> which maps to a <b>UINT8</b>.

Possible values:

<table>
<tr>
<th>IPsec authentication configuration</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_CONFIG_HMAC_MD5_96"></a><a id="ipsec_auth_config_hmac_md5_96"></a><dl>
<dt><b>IPSEC_AUTH_CONFIG_HMAC_MD5_96</b></dt>
</dl>
</td>
<td width="60%">
HMAC (Hash Message Authentication Code) secret key authentication algorithm.

MD5 (Message Digest) data integrity and data origin authentication  algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_CONFIG_HMAC_SHA_1_96"></a><a id="ipsec_auth_config_hmac_sha_1_96"></a><dl>
<dt><b>IPSEC_AUTH_CONFIG_HMAC_SHA_1_96</b></dt>
</dl>
</td>
<td width="60%">
HMAC secret key authentication algorithm. 

SHA-1 (Secure Hash Algorithm) data integrity and data origin authentication  algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_CONFIG_HMAC_SHA_256_128"></a><a id="ipsec_auth_config_hmac_sha_256_128"></a><dl>
<dt><b>IPSEC_AUTH_CONFIG_HMAC_SHA_256_128</b></dt>
</dl>
</td>
<td width="60%">
 HMAC secret key authentication algorithm. 

SHA-256 data integrity and data origin authentication  algorithm.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_CONFIG_GCM_AES_128"></a><a id="ipsec_auth_config_gcm_aes_128"></a><dl>
<dt><b>IPSEC_AUTH_CONFIG_GCM_AES_128</b></dt>
</dl>
</td>
<td width="60%">
 GCM (Galois Counter Mode) secret key authentication algorithm. 

AES(Advanced Encryption Standard) data integrity and data origin authentication  algorithm, with 128-bit key.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_CONFIG_GCM_AES_192"></a><a id="ipsec_auth_config_gcm_aes_192"></a><dl>
<dt><b>IPSEC_AUTH_CONFIG_GCM_AES_192</b></dt>
</dl>
</td>
<td width="60%">
 GCM secret key authentication algorithm. 

AES data integrity and data origin authentication  algorithm, with 192-bit key.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_CONFIG_GCM_AES_256"></a><a id="ipsec_auth_config_gcm_aes_256"></a><dl>
<dt><b>IPSEC_AUTH_CONFIG_GCM_AES_256</b></dt>
</dl>
</td>
<td width="60%">
 GCM secret key authentication algorithm. 

AES data integrity and data origin authentication  algorithm, with 256-bit key.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
</table>

## -remarks

<b>IPSEC_AUTH_TRANSFORM_ID0</b> is a specific implementation of IPSEC_AUTH_TRANSFORM_ID. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>