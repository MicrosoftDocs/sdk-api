---
UID: NS:wincrypt._CMSG_KEY_AGREE_RECIPIENT_INFO
title: CMSG_KEY_AGREE_RECIPIENT_INFO (wincrypt.h)
description: Contains information used for key agreement algorithms.
helpviewer_keywords: ["*PCMSG_KEY_AGREE_RECIPIENT_INFO","CMSG_KEY_AGREE_ORIGINATOR_CERT","CMSG_KEY_AGREE_ORIGINATOR_PUBLIC_KEY","CMSG_KEY_AGREE_RECIPIENT_INFO","CMSG_KEY_AGREE_RECIPIENT_INFO structure [Security]","PCMSG_KEY_AGREE_RECIPIENT_INFO","PCMSG_KEY_AGREE_RECIPIENT_INFO structure pointer [Security]","_crypto2_cmsg_key_agree_recipient_info","security.cmsg_key_agree_recipient_info","wincrypt/CMSG_KEY_AGREE_RECIPIENT_INFO","wincrypt/PCMSG_KEY_AGREE_RECIPIENT_INFO"]
old-location: security\cmsg_key_agree_recipient_info.htm
tech.root: security
ms.assetid: d29d04d6-065e-4bb7-843b-f563643eeb4c
ms.date: 12/05/2018
ms.keywords: '*PCMSG_KEY_AGREE_RECIPIENT_INFO, CMSG_KEY_AGREE_ORIGINATOR_CERT, CMSG_KEY_AGREE_ORIGINATOR_PUBLIC_KEY, CMSG_KEY_AGREE_RECIPIENT_INFO, CMSG_KEY_AGREE_RECIPIENT_INFO structure [Security], PCMSG_KEY_AGREE_RECIPIENT_INFO, PCMSG_KEY_AGREE_RECIPIENT_INFO structure pointer [Security], _crypto2_cmsg_key_agree_recipient_info, security.cmsg_key_agree_recipient_info, wincrypt/CMSG_KEY_AGREE_RECIPIENT_INFO, wincrypt/PCMSG_KEY_AGREE_RECIPIENT_INFO'
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
req.typenames: CMSG_KEY_AGREE_RECIPIENT_INFO, *PCMSG_KEY_AGREE_RECIPIENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_KEY_AGREE_RECIPIENT_INFO
 - wincrypt/_CMSG_KEY_AGREE_RECIPIENT_INFO
 - PCMSG_KEY_AGREE_RECIPIENT_INFO
 - wincrypt/PCMSG_KEY_AGREE_RECIPIENT_INFO
 - CMSG_KEY_AGREE_RECIPIENT_INFO
 - wincrypt/CMSG_KEY_AGREE_RECIPIENT_INFO
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
 - CMSG_KEY_AGREE_RECIPIENT_INFO
---

# CMSG_KEY_AGREE_RECIPIENT_INFO structure


## -description

The <b>CMSG_KEY_AGREE_RECIPIENT_INFO</b> structure contains information used for key agreement algorithms.

## -struct-fields

### -field dwVersion

A <b>DWORD</b> that indicates the version of the structure. Always set to three.

### -field dwOriginatorChoice

A <b>DWORD</b> that indicates the key identifier to use. 


This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ORIGINATOR_CERT"></a><a id="cmsg_key_agree_originator_cert"></a><dl>
<dt><b>CMSG_KEY_AGREE_ORIGINATOR_CERT</b></dt>
</dl>
</td>
<td width="60%">
OriginatorCertId

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_KEY_AGREE_ORIGINATOR_PUBLIC_KEY"></a><a id="cmsg_key_agree_originator_public_key"></a><dl>
<dt><b>CMSG_KEY_AGREE_ORIGINATOR_PUBLIC_KEY</b></dt>
</dl>
</td>
<td width="60%">
OriginatorPublicKeyInfo

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.OriginatorCertId

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a>  that identifies the public key of the message originator.

### -field DUMMYUNIONNAME.OriginatorPublicKeyInfo

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key of the message originator.

### -field UserKeyingMaterial

 A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> that indicates that a different key is generated each time the same two parties generate a pair of keys. The sender provides the bits of this <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> with some key agreement algorithms. This member can be <b>NULL</b>.

### -field KeyEncryptionAlgorithm

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> that identifies the key-encryption algorithm and any associated parameters used to encrypt the content encryption key.

### -field cRecipientEncryptedKeys

The number of elements in the <b>rgpRecipientEncryptedKeys</b> array.

### -field rgpRecipientEncryptedKeys

The address of an array of <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_recipient_encrypted_key_info">CMSG_RECIPIENT_ENCRYPTED_KEY_INFO</a> structures that contains information about the key recipients. The <b>cRecipientEncryptedKeys</b> member contains the number of elements in this array.