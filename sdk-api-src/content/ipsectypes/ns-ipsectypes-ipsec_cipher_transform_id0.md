---
UID: NS:ipsectypes.IPSEC_CIPHER_TRANSFORM_ID0_
title: IPSEC_CIPHER_TRANSFORM_ID0 (ipsectypes.h)
description: Specifies information used to uniquely identify the encryption algorithm used in an IPsec SA.
helpviewer_keywords: ["IPSEC_CIPHER_CONFIG_CBC_3DES","IPSEC_CIPHER_CONFIG_CBC_AES_128","IPSEC_CIPHER_CONFIG_CBC_AES_192","IPSEC_CIPHER_CONFIG_CBC_AES_256","IPSEC_CIPHER_CONFIG_CBC_DES","IPSEC_CIPHER_CONFIG_GCM_AES_128","IPSEC_CIPHER_CONFIG_GCM_AES_192","IPSEC_CIPHER_CONFIG_GCM_AES_256","IPSEC_CIPHER_TRANSFORM_ID0","IPSEC_CIPHER_TRANSFORM_ID0 structure [Filtering]","fwp.ipsec_cipher_transform_id0_struct","ipsectypes/IPSEC_CIPHER_TRANSFORM_ID0"]
old-location: fwp\ipsec_cipher_transform_id0_struct.htm
tech.root: fwp
ms.assetid: fc58606b-18a4-49ab-87bb-a6846b81520b
ms.date: 12/05/2018
ms.keywords: IPSEC_CIPHER_CONFIG_CBC_3DES, IPSEC_CIPHER_CONFIG_CBC_AES_128, IPSEC_CIPHER_CONFIG_CBC_AES_192, IPSEC_CIPHER_CONFIG_CBC_AES_256, IPSEC_CIPHER_CONFIG_CBC_DES, IPSEC_CIPHER_CONFIG_GCM_AES_128, IPSEC_CIPHER_CONFIG_GCM_AES_192, IPSEC_CIPHER_CONFIG_GCM_AES_256, IPSEC_CIPHER_TRANSFORM_ID0, IPSEC_CIPHER_TRANSFORM_ID0 structure [Filtering], fwp.ipsec_cipher_transform_id0_struct, ipsectypes/IPSEC_CIPHER_TRANSFORM_ID0
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
req.typenames: IPSEC_CIPHER_TRANSFORM_ID0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_CIPHER_TRANSFORM_ID0_
 - ipsectypes/IPSEC_CIPHER_TRANSFORM_ID0_
 - IPSEC_CIPHER_TRANSFORM_ID0
 - ipsectypes/IPSEC_CIPHER_TRANSFORM_ID0
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
 - IPSEC_CIPHER_TRANSFORM_ID0
---

# IPSEC_CIPHER_TRANSFORM_ID0 structure


## -description

The <b>IPSEC_CIPHER_TRANSFORM_ID0</b> structure specifies information used to uniquely identify the encryption algorithm used in an IPsec SA.

## -struct-fields

### -field cipherType

The type of the encryption algorithm as specified by [IPSEC_CIPHER_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_cipher_type).

### -field cipherConfig

Additional configuration information for the encryption algorithm as specified by <b>IPSEC_CIPHER_CONFIG</b> which maps to a <b>UINT8</b>.

Possible values:

<table>
<tr>
<th>IPsec encryption configuration</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_CBC_DES"></a><a id="ipsec_cipher_config_cbc_des"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_CBC_DES</b></dt>
</dl>
</td>
<td width="60%">
DES (Data Encryption Standard) algorithm. 

CBC (Cipher Block Chaining) mode of operation.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_CBC_3DES"></a><a id="ipsec_cipher_config_cbc_3des"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_CBC_3DES</b></dt>
</dl>
</td>
<td width="60%">
3DES algorithm. 

CBC mode of operation.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_CBC_AES_128"></a><a id="ipsec_cipher_config_cbc_aes_128"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_CBC_AES_128</b></dt>
</dl>
</td>
<td width="60%">
AES-128 (Advanced Encryption Standard) algorithm. 

CBC mode of operation.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_CBC_AES_192"></a><a id="ipsec_cipher_config_cbc_aes_192"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_CBC_AES_192</b></dt>
</dl>
</td>
<td width="60%">
AES-192 algorithm. 

CBC mode of operation.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_CBC_AES_256"></a><a id="ipsec_cipher_config_cbc_aes_256"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_CBC_AES_256</b></dt>
</dl>
</td>
<td width="60%">
AES-256 algorithm. 

CBC mode of operation.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_GCM_AES_128"></a><a id="ipsec_cipher_config_gcm_aes_128"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_GCM_AES_128</b></dt>
</dl>
</td>
<td width="60%">
AES-128 algorithm. 

GCM (Galois Counter Mode) mode of operation.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_GCM_AES_192"></a><a id="ipsec_cipher_config_gcm_aes_192"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_GCM_AES_192</b></dt>
</dl>
</td>
<td width="60%">
AES-192 algorithm. 

GCM (Galois Counter Mode) mode of operation.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_CONFIG_GCM_AES_256"></a><a id="ipsec_cipher_config_gcm_aes_256"></a><dl>
<dt><b>IPSEC_CIPHER_CONFIG_GCM_AES_256</b></dt>
</dl>
</td>
<td width="60%">
AES-256 algorithm.

GCM (Galois Counter Mode) mode of operation.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
</table>

## -remarks

<b>IPSEC_CIPHER_TRANSFORM_ID0</b> is a specific implementation of IPSEC_CIPHER_TRANSFORM_ID. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_CIPHER_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_cipher_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>