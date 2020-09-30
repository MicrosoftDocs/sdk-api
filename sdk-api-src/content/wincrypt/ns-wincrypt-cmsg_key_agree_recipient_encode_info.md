---
UID: NS:wincrypt._CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
title: CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO (wincrypt.h)
description: Contains information about a message recipient that is using key agreement key management.
helpviewer_keywords: ["*PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO","CMSG_KEY_AGREE_EPHEMERAL_KEY_CHOICE","CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO","CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO structure [Security]","CMSG_KEY_AGREE_STATIC_KEY_CHOICE","PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO","PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO structure pointer [Security]","_crypto2_cmsg_key_agree_recipient_encode_info","security.cmsg_key_agree_recipient_encode_info","wincrypt/CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO","wincrypt/PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO"]
old-location: security\cmsg_key_agree_recipient_encode_info.htm
tech.root: security
ms.assetid: f8691df7-3cc1-48cb-8787-84c7046b280f
ms.date: 12/05/2018
ms.keywords: '*PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO, CMSG_KEY_AGREE_EPHEMERAL_KEY_CHOICE, CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO, CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO structure [Security], CMSG_KEY_AGREE_STATIC_KEY_CHOICE, PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO, PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO structure pointer [Security], _crypto2_cmsg_key_agree_recipient_encode_info, security.cmsg_key_agree_recipient_encode_info, wincrypt/CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO, wincrypt/PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO'
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
req.typenames: CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO, *PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
 - wincrypt/_CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
 - PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
 - wincrypt/PCMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
 - CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
 - wincrypt/CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
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
 - CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO
---

# CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO structure


## -description

The <b>CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO</b> structure contains information about a message recipient that is using key agreement key management.This structure is used with the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_recipient_encode_info">CMSG_RECIPIENT_ENCODE_INFO</a> structure.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field KeyEncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used for encryption.

For ECC recipients, the <b>pszObjId</b> member of the  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure should be set to szOID_DH_SINGLE_PASS_STDDH_SHA1_KDF with the <b>dwKeyChoice</b> member of this <b>CMSG_KEY_AGREE_RECIPIENT_ENCODE_INFO</b> structure set to CMSG_KEY_AGREE_EPHEMERAL_KEY_CHOICE.

### -field pvKeyEncryptionAuxInfo

This member is not currently used. It must be set to <b>NULL</b>.

### -field KeyWrapAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used for key wrapping.

### -field pvKeyWrapAuxInfo

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc2_aux_info">CMSG_RC2_AUX_INFO</a> structure that specifies the key wrapping bit length. This member is only used if the <b>KeyWrapAlgorithm</b> member specifies an RC2 algorithm. If <b>KeyWrapAlgorithm</b> specifies an algorithm other than an RC2 algorithm, this member is not used and must be <b>NULL</b>.

### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) obtained by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function. This member is optional and can be <b>NULL</b>.This member's data type is <b>HCRYPTPROV</b>.

### -field dwKeySpec

This member is not currently used.

### -field dwKeyChoice

Indicates the type of key agreement. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_EPHEMERAL_KEY_CHOICE"></a><a id="cmsg_key_agree_ephemeral_key_choice"></a><dl>
<dt><b>CMSG_KEY_AGREE_EPHEMERAL_KEY_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
Create a temporary <a href="/windows/desktop/SecGloss/p-gly">public/private key pair</a> to encrypt the content encryption key.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_STATIC_KEY_CHOICE"></a><a id="cmsg_key_agree_static_key_choice"></a><dl>
<dt><b>CMSG_KEY_AGREE_STATIC_KEY_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
This value is not currently used.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pEphemeralAlgorithm

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the ephemeral public key algorithm and parameters. This member is used when the <b>dwKeyChoice</b> member contains <b>CMSG_KEY_AGREE_EPHEMERAL_KEY_CHOICE</b>.

### -field DUMMYUNIONNAME.pSenderId

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure. This member is used when the <b>dwKeyChoice</b> member contains <b>CMSG_KEY_AGREE_STATIC_KEY_CHOICE</b>. This member is not currently used.

### -field UserKeyingMaterial

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains user keying material (UKM) provided by the sender to ensure that a different key is generated each time the same two parties generate a pair-wise key. This member is optional and all members should be set to zero if not used.

### -field cRecipientEncryptedKeys

The number of elements in the <b>rgpRecipientEncryptedKeys</b> array.

### -field rgpRecipientEncryptedKeys

An array of  <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_recipient_encrypted_key_encode_info">CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO</a> structures, one for each recipient to receive this key agreement key. The <b>cRecipientEncryptedKeys</b> member contains the number of elements in this structure.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc2_aux_info">CMSG_RC2_AUX_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_recipient_encode_info">CMSG_RECIPIENT_ENCODE_INFO</a>



<a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_recipient_encrypted_key_encode_info">CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>