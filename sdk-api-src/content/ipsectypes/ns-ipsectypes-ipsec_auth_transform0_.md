---
UID: NS:ipsectypes.IPSEC_AUTH_TRANSFORM0_
title: IPSEC_AUTH_TRANSFORM0_
author: windows-sdk-content
description: Specifies hash specific information for an SA transform.
old-location: fwp\ipsec_auth_transform0_struct.htm
old-project: FWP
ms.assetid: 26464393-7dc4-4a94-af46-25148c61bdb5
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_AUTH_TRANSFORM0, IPSEC_AUTH_TRANSFORM0 structure [Filtering], IPSEC_AUTH_TRANSFORM0_, IPSEC_AUTH_TRANSFORM_ID_GCM_AES_128, IPSEC_AUTH_TRANSFORM_ID_GCM_AES_192, IPSEC_AUTH_TRANSFORM_ID_GCM_AES_256, IPSEC_AUTH_TRANSFORM_ID_HMAC_MD5_96, IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_1_96, IPSEC_AUTH_TRANSFORM_ID_HMAC_SHA_256_128, fwp.ipsec_auth_transform0_struct, ipsectypes/IPSEC_AUTH_TRANSFORM0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: IPSEC_AUTH_TRANSFORM0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_AUTH_TRANSFORM0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

