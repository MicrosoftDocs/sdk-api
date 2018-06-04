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

# _SCHANNEL_ALG structure


## -description


The <b>SCHANNEL_ALG</b> structure contains algorithm and key size information. It is used as the structure passed as <i>pbData</i> in <a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a> when <i>dwParam</i> is set to KP_SCHANNEL_ALG.


## -struct-fields




### -field dwUse

Indicates the use of derived keys. The following values can be used. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCHANNEL_MAC_KEY"></a><a id="schannel_mac_key"></a><dl>
<dt><b>SCHANNEL_MAC_KEY</b></dt>
</dl>
</td>
<td width="60%">
Derive keys to create or verify SSL MAC signatures.

</td>
</tr>
<tr>
<td width="40%"><a id="SCHANNEL_ENC_KEY"></a><a id="schannel_enc_key"></a><dl>
<dt><b>SCHANNEL_ENC_KEY</b></dt>
</dl>
</td>
<td width="60%">
Derive keys to encrypt or decrypt data.

</td>
</tr>
</table>
 


### -field Algid

Algorithms used with the derived keys. Note that no algorithm will be specified unless earlier obtained from the CSP by enumeration. 




SCHANNEL_MAC_KEYs can be either MD5 or SHA.

SCHANNEL_ENC_KEYs can be RC4, DES, 3DES, or RC2.


### -field cBits

Size in bits of the derived keys.


### -field dwFlags

This flag can be set to INTERNATIONAL_USAGE (0x00000001), indicating that derived keys must follow SSL export rules.


### -field dwReserved

Reserved for future use. Should be set to zero.

