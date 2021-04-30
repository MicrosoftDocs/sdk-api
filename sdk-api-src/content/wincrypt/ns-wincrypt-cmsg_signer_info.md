---
UID: NS:wincrypt._CMSG_SIGNER_INFO
title: CMSG_SIGNER_INFO (wincrypt.h)
description: The CMSG_SIGNER_INFO structure contains the content of the PKCS
helpviewer_keywords: ["*PCMSG_SIGNER_INFO","CMSG_SIGNER_INFO","CMSG_SIGNER_INFO structure [Security]","PCMSG_SIGNER_INFO","PCMSG_SIGNER_INFO structure pointer [Security]","_crypto2_cmsg_signer_info","security.cmsg_signer_info","wincrypt/CMSG_SIGNER_INFO","wincrypt/PCMSG_SIGNER_INFO"]
old-location: security\cmsg_signer_info.htm
tech.root: security
ms.assetid: eae631d2-5e5f-4964-b079-9692831b34fc
ms.date: 12/05/2018
ms.keywords: '*PCMSG_SIGNER_INFO, CMSG_SIGNER_INFO, CMSG_SIGNER_INFO structure [Security], PCMSG_SIGNER_INFO, PCMSG_SIGNER_INFO structure pointer [Security], _crypto2_cmsg_signer_info, security.cmsg_signer_info, wincrypt/CMSG_SIGNER_INFO, wincrypt/PCMSG_SIGNER_INFO'
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
req.typenames: CMSG_SIGNER_INFO, *PCMSG_SIGNER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_SIGNER_INFO
 - wincrypt/_CMSG_SIGNER_INFO
 - PCMSG_SIGNER_INFO
 - wincrypt/PCMSG_SIGNER_INFO
 - CMSG_SIGNER_INFO
 - wincrypt/CMSG_SIGNER_INFO
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
 - CMSG_SIGNER_INFO
---

# CMSG_SIGNER_INFO structure


## -description

The <b>CMSG_SIGNER_INFO</b> structure contains the content of the PKCS #7 defined SignerInfo in signed messages. In decoding a received message, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a> is called for each signer to get a <b>CMSG_SIGNER_INFO</b> structure.

## -struct-fields

### -field dwVersion

The version of this structure.

### -field Issuer

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure that contains the issuer of a certificate with the public key needed to verify a signature.

### -field SerialNumber

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the serial number of the certificate that contains the public key needed to verify a signature. For more information, see 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>.

### -field HashAlgorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure specifying the algorithm used in generating the hash of a message.

### -field HashEncryptionAlgorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure specifying the algorithm used to encrypt the hash.

### -field EncryptedHash

A
						<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> that contains the encrypted hash of the message, the signature.

### -field AuthAttrs

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure containing authenticated attributes of the signer.

### -field UnauthAttrs

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure containing unauthenticated attributes of the signer.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>