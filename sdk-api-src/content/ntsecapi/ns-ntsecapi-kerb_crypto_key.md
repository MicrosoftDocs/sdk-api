---
UID: NS:ntsecapi.KERB_CRYPTO_KEY
title: KERB_CRYPTO_KEY (ntsecapi.h)
description: Contains information about a Kerberos cryptographic session key.
helpviewer_keywords: ["*PKERB_CRYPTO_KEY","KERB_CRYPTO_KEY","KERB_CRYPTO_KEY structure [Security]","KERB_ETYPE_DES_CBC_CRC","KERB_ETYPE_DES_CBC_MD4","KERB_ETYPE_DES_CBC_MD5","KERB_ETYPE_NULL","KERB_ETYPE_RC4_HMAC_NT","KERB_ETYPE_RC4_MD4","PKERB_CRYPTO_KEY","PKERB_CRYPTO_KEY structure pointer [Security]","_lsa_kerb_crypto_key","ntsecapi/KERB_CRYPTO_KEY","ntsecapi/PKERB_CRYPTO_KEY","security.kerb_crypto_key"]
old-location: security\kerb_crypto_key.htm
tech.root: security
ms.assetid: ac7ea61c-b1e0-4dc0-931e-81bb6fd74888
ms.date: 12/05/2018
ms.keywords: '*PKERB_CRYPTO_KEY, KERB_CRYPTO_KEY, KERB_CRYPTO_KEY structure [Security], KERB_ETYPE_DES_CBC_CRC, KERB_ETYPE_DES_CBC_MD4, KERB_ETYPE_DES_CBC_MD5, KERB_ETYPE_NULL, KERB_ETYPE_RC4_HMAC_NT, KERB_ETYPE_RC4_MD4, PKERB_CRYPTO_KEY, PKERB_CRYPTO_KEY structure pointer [Security], _lsa_kerb_crypto_key, ntsecapi/KERB_CRYPTO_KEY, ntsecapi/PKERB_CRYPTO_KEY, security.kerb_crypto_key'
req.header: ntsecapi.h
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
req.typenames: KERB_CRYPTO_KEY, *PKERB_CRYPTO_KEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KERB_CRYPTO_KEY
 - ntsecapi/KERB_CRYPTO_KEY
 - PKERB_CRYPTO_KEY
 - ntsecapi/PKERB_CRYPTO_KEY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_CRYPTO_KEY
---

# KERB_CRYPTO_KEY structure


## -description

The <b>KERB_CRYPTO_KEY</b> structure contains information about a <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> cryptographic <a href="/windows/desktop/SecGloss/s-gly">session key</a>.

## -struct-fields

### -field KeyType

Indicates the type of <a href="/windows/desktop/SecGloss/s-gly">session key</a> stored in the structure. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_DES_CBC_CRC"></a><a id="kerb_etype_des_cbc_crc"></a><dl>
<dt><b>KERB_ETYPE_DES_CBC_CRC</b></dt>
</dl>
</td>
<td width="60%">
Use <a href="/windows/desktop/SecGloss/d-gly">DES</a> encryption in <a href="/windows/desktop/SecGloss/c-gly">cipher-block-chaining</a> mode with a CRC-32 checksum.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_DES_CBC_MD4"></a><a id="kerb_etype_des_cbc_md4"></a><dl>
<dt><b>KERB_ETYPE_DES_CBC_MD4</b></dt>
</dl>
</td>
<td width="60%">
Use DES encryption in cipher-block-chaining mode with a MD4 checksum.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_DES_CBC_MD5"></a><a id="kerb_etype_des_cbc_md5"></a><dl>
<dt><b>KERB_ETYPE_DES_CBC_MD5</b></dt>
</dl>
</td>
<td width="60%">
Use DES encryption in cipher-block-chaining mode with a MD5 checksum.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_NULL"></a><a id="kerb_etype_null"></a><dl>
<dt><b>KERB_ETYPE_NULL</b></dt>
</dl>
</td>
<td width="60%">
Use no encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_RC4_HMAC_NT"></a><a id="kerb_etype_rc4_hmac_nt"></a><dl>
<dt><b>KERB_ETYPE_RC4_HMAC_NT</b></dt>
</dl>
</td>
<td width="60%">
Use the RC4 <a href="/windows/desktop/SecGloss/s-gly">stream cipher</a> with a <a href="/windows/desktop/SecGloss/h-gly">hash</a>-based <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC).

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_RC4_MD4"></a><a id="kerb_etype_rc4_md4"></a><dl>
<dt><b>KERB_ETYPE_RC4_MD4</b></dt>
</dl>
</td>
<td width="60%">
Use the RC4 stream cipher with the MD4 hash function.

</td>
</tr>
</table>
 

Values greater than 127 are reserved for local values and may change without notice.

### -field Length

Specifies the length, in bytes, of the cryptographic <a href="/windows/desktop/SecGloss/s-gly">session key</a>.

### -field Value

Contains the cryptographic session key.