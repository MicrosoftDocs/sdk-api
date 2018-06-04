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

# IPSEC_CIPHER_TRANSFORM0_ structure


## -description


The <b>IPSEC_CIPHER_TRANSFORM0</b> structure is used to store encryption specific information for an SA transform in an IPsec quick mode policy.


## -struct-fields




### -field cipherTransformId

The identifier of the encryption algorithm as specified by <a href="https://msdn.microsoft.com/fc58606b-18a4-49ab-87bb-a6846b81520b">IPSEC_CIPHER_TRANSFORM_ID0</a>.

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_CBC_DES"></a><a id="ipsec_cipher_transform_id_cbc_des"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_CBC_DES</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_DES,
   IPSEC_CIPHER_CONFIG_CBC_DES


</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_CBC_3DES"></a><a id="ipsec_cipher_transform_id_cbc_3des"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_CBC_3DES</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_3DES,
   IPSEC_CIPHER_CONFIG_CBC_3DES


</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_AES_128"></a><a id="ipsec_cipher_transform_id_aes_128"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_AES_128</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_AES_128,
   IPSEC_CIPHER_CONFIG_CBC_AES_128


</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_AES_192"></a><a id="ipsec_cipher_transform_id_aes_192"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_AES_192</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_AES_192,
   IPSEC_CIPHER_CONFIG_CBC_AES_192


</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_AES_256_"></a><a id="ipsec_cipher_transform_id_aes_256_"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_AES_256 </b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_AES_256,
   IPSEC_CIPHER_CONFIG_CBC_AES_256


</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_GCM_AES_128_"></a><a id="ipsec_cipher_transform_id_gcm_aes_128_"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_GCM_AES_128 </b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_AES_128,
   IPSEC_CIPHER_CONFIG_GCM_AES_128


<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_GCM_AES_192"></a><a id="ipsec_cipher_transform_id_gcm_aes_192"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_GCM_AES_192</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_AES_192,
   IPSEC_CIPHER_CONFIG_GCM_AES_192


<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TRANSFORM_ID_GCM_AES_256"></a><a id="ipsec_cipher_transform_id_gcm_aes_256"></a><dl>
<dt><b>IPSEC_CIPHER_TRANSFORM_ID_GCM_AES_256</b></dt>
</dl>
</td>
<td width="60%">
   IPSEC_CIPHER_TYPE_AES_256,
   IPSEC_CIPHER_CONFIG_GCM_AES_256


<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>
</td>
</tr>
</table>
 


### -field cryptoModuleId

Unused parameter, always set this to <b>NULL</b>.


## -remarks



<b>IPSEC_CIPHER_TRANSFORM0</b> is a specific implementation of IPSEC_CIPHER_TRANSFORM. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/fc58606b-18a4-49ab-87bb-a6846b81520b">IPSEC_CIPHER_TRANSFORM_ID0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

