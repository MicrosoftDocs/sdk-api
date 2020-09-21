---
UID: NS:wincrypt._SCHANNEL_ALG
title: SCHANNEL_ALG (wincrypt.h)
description: The SCHANNEL_ALG structure contains algorithm and key size information. It is used as the structure passed as pbData in CryptSetKeyParam when dwParam is set to KP_SCHANNEL_ALG.
helpviewer_keywords: ["*PSCHANNEL_ALG","PSCHANNEL_ALG","PSCHANNEL_ALG structure pointer [Security]","SCHANNEL_ALG","SCHANNEL_ALG structure [Security]","SCHANNEL_ENC_KEY","SCHANNEL_MAC_KEY","_crypto2_schannel_alg","security.schannel_alg","wincrypt/PSCHANNEL_ALG","wincrypt/SCHANNEL_ALG"]
old-location: security\schannel_alg.htm
tech.root: security
ms.assetid: 55afebf4-8872-42a1-847f-ff0240c2be20
ms.date: 12/05/2018
ms.keywords: '*PSCHANNEL_ALG, PSCHANNEL_ALG, PSCHANNEL_ALG structure pointer [Security], SCHANNEL_ALG, SCHANNEL_ALG structure [Security], SCHANNEL_ENC_KEY, SCHANNEL_MAC_KEY, _crypto2_schannel_alg, security.schannel_alg, wincrypt/PSCHANNEL_ALG, wincrypt/SCHANNEL_ALG'
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
req.typenames: SCHANNEL_ALG, *PSCHANNEL_ALG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHANNEL_ALG
 - wincrypt/_SCHANNEL_ALG
 - PSCHANNEL_ALG
 - wincrypt/PSCHANNEL_ALG
 - SCHANNEL_ALG
 - wincrypt/SCHANNEL_ALG
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
 - SCHANNEL_ALG
---

# SCHANNEL_ALG structure


## -description

The <b>SCHANNEL_ALG</b> structure contains algorithm and key size information. It is used as the structure passed as <i>pbData</i> in <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a> when <i>dwParam</i> is set to KP_SCHANNEL_ALG.

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