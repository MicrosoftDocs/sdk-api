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

# IPSEC_CIPHER_TRANSFORM_ID0_ structure


## -description



		The <b>IPSEC_CIPHER_TRANSFORM_ID0</b> structure specifies information used to uniquely identify the encryption algorithm used in an IPsec SA.


## -struct-fields




### -field cipherType

The type of the encryption algorithm as specified by <a href="https://msdn.microsoft.com/88bcd239-83a6-4bc6-b9c8-2416c91ee4c4">IPSEC_CIPHER_TYPE</a>.


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



<b>IPSEC_CIPHER_TRANSFORM_ID0</b> is a specific implementation of IPSEC_CIPHER_TRANSFORM_ID. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/88bcd239-83a6-4bc6-b9c8-2416c91ee4c4">IPSEC_CIPHER_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

