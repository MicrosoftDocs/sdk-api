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

# IPSEC_AUTH_TRANSFORM0_ structure


## -description


The <b>IPSEC_AUTH_TRANSFORM0</b> structure specifies hash specific information for an SA transform.


## -struct-fields




### -field authTransformId

The identifier of the hash algorithm as specified by <a href="https://msdn.microsoft.com/b8474e98-451d-4347-9369-367f16f83cf6">IPSEC_AUTH_TRANSFORM_ID0</a>.

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_TRANSFORM_ID_HMAC_MD5_96"></a><a id="ipsec_auth_transform_id_hmac_md5_96"></a><dl>
<dt><b>IPSEC_AUTH_TRANSFORM_ID_HMAC_MD5_96</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_AUTH_MD5,
   IPSEC_AUTH_CONFIG_HMAC_MD5_96

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_1_96"></a><a id="ipsec_auth_transform_id_hmac_sha_1_96"></a><dl>
<dt><b>IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_1_96</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_AUTH_SHA_1,
   IPSEC_AUTH_CONFIG_HMAC_SHA_1_96


</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_256_128"></a><a id="ipsec_auth_transform_id_hmac_sha_256_128"></a><dl>
<dt><b>IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_256_128</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_AUTH_SHA_256,
   IPSEC_AUTH_CONFIG_HMAC_SHA_256_128


<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_TRANSFORM_ID_GCM_AES_128"></a><a id="ipsec_auth_transform_id_gcm_aes_128"></a><dl>
<dt><b>IPSEC_AUTH_TRANSFORM_ID_GCM_AES_128</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_AUTH_AES_128,
   IPSEC_AUTH_CONFIG_GCM_AES_128


<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_TRANSFORM_ID_GCM_AES_192"></a><a id="ipsec_auth_transform_id_gcm_aes_192"></a><dl>
<dt><b>IPSEC_AUTH_TRANSFORM_ID_GCM_AES_192</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_AUTH_AES_192,
   IPSEC_AUTH_CONFIG_GCM_AES_192


<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_AUTH_TRANSFORM_ID_GCM_AES_256"></a><a id="ipsec_auth_transform_id_gcm_aes_256"></a><dl>
<dt><b>IPSEC_AUTH_TRANSFORM_ID_GCM_AES_256</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_AUTH_AES_256,
   IPSEC_AUTH_CONFIG_GCM_AES_256

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
</table>
 


### -field cryptoModuleId

Unused parameter, always set this to <b>NULL</b>.


## -remarks



<b>IPSEC_AUTH_TRANSFORM0</b> is a specific implementation of IPSEC_AUTH_TRANSFORM. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/b8474e98-451d-4347-9369-367f16f83cf6">IPSEC_AUTH_TRANSFORM_ID0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

